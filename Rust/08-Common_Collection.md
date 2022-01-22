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

