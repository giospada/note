# Common Collection

## Vec

vettore è una struttura generica dichiarata `Vec<T>` 

### Funzioni e Metodi

- `new()` è una **funzione** che serve per prendere in input un altro 
- `vec![el1,...eln]` è una **macro** che serve per creare 
- `push(T el)` è un **metodo** che aggiunge un elemento al vettore (solo se il vettore è definito con la praola `mut`)
- `get(int index)` è un **metodo** che ritorna un `Option<T>` così da non andare in segment fault se viene richiesto un valore fuori dal range 
- `[]` è un metodo più rischioso di get per accedere ad un array


### Borrowing

Per le regole del borrowing valgono anche per i vettori per esempio non possiamo modificare un vettore mentre abbiamo un reference immutabile.


### Interating values

```rust
let v = vec![100, 32, 57];
for i in &v {
    println!("{}", i);
}
```
```rust
let mut v = vec![100, 32, 57];
for i in &mut v {
    //bisogna utilizzare il dereference operator
    *i += 50;
}
```
### Enum

si possono creare delle enum per storare in un vettore tipi differenti.

## String

Sono codificate in `UTF-8`, quindi sono complicate da lavorarci.


### Metodi

- `new()` è una **funzione** che crea una stringa
- `from(str)` è un **funzione** che crea una stringa da una presa in input
- `push_str(str)` è un **metodo** utilizzabile solo se è dichiarato mut (prende l'ovnership)

### Problemi con le stringhe

I problemi diciamo che derivano dal fatto che le stringhe siano rappresentate come un vettore di 8 bit

#### Indirizzamento

Indicizzare le stringhe è complicato perchè la codifica UTF-8 usa dinamicamente da uno a 4 byte.

<details>
<summary>
esempi di codifiche in byte di stringhe
</summary>

```text
[224, 164, 168, 224, 164, 174, 224, 164, 184, 224, 165, 141, 224, 164, 164,
224, 165, 135]
```
è uguale a  
```text
['न', 'म', 'स', '्', 'त', 'े']
```
che è uguale a  
```text
["न", "म", "स्", "ते"]
```
</details>

si può iterare sulle strighe con `chars()`

```rust
fn main() {
    for c in "नमस्ते".chars() {
        println!("{}", c);
    }
}
```

#### Concatenazione

la concatenazione può essere un po' triky per come e definito il metodo `+` in string, questo metodo prende il borrowing della prima stringa e il reference di un altra in input facendo diventare inutilizzabile la prima stringa.


```rust
fn main() {
    let s1 = String::from("Hello, ");
    let s2 = String::from("world!");
    let s3 = s1 + &s2; // note s1 has been moved here and can no longer be used
}
```

in alternativa si può utilizzare la macro **format** che è più user frendly.

```rust
fn main() {
    let s1 = String::from("tic");
    let s2 = String::from("tac");
    let s3 = String::from("toe");

    let s = format!("{}-{}-{}", s1, s2, s3);
}
```


### HashMap

bisogna includerla a differenza delle altre due strutture

## Metodi

può essere anche inizializzata con un vettore di turple

- `new()`  **funzione** che crea una nuova istanza
- `insert(key,val)` **metodo** che inserisce un valore (deve essere definita mut) se il valre esiste viene sovrascritto
- `entry(Key)` **metodo** che restituisce una enum `Entry` (che indica che il valore può esistere o non esistere) si può utilizzare in comibinazione con `or_insert` che permette di aggiungere l'elemento se non esiste
- `get(key)->Option<&VAl>` **metodo** per accedere agli elementi

### Iterazione

```rust
fn main() {
    use std::collections::HashMap;

    let mut scores = HashMap::new();

    scores.insert(String::from("Blue"), 10);
    scores.insert(String::from("Yellow"), 50);

    for (key, value) in &scores {
        println!("{}: {}", key, value);
    }
}
```

## Updating values


```rust
fn main() {
    use std::collections::HashMap;

    let text = "hello world wonderful world";

    let mut map = HashMap::new();

    for word in text.split_whitespace() {
        let count = map.entry(word).or_insert(0);
        *count += 1;
    }

    println!("{:?}", map);
}
```



