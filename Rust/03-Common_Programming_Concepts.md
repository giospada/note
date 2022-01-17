# 03-Common_Programming_Concepts

## Variabili

### Variabili mutabili e immutabili

le variabili in rust sono **immutabili di default** per renderle mutabili è necessaria la parola chiave `mut`

<details>
<summary>
esempio
</summary>

errore di compilazione:
```rust
fn main() {
    let x = 5;
    println!("The value of x is: {}", x);
    x = 6;
    println!("The value of x is: {}", x);
}
```

codice giusto:
```rust
fn main() {
    let mut x = 5;
    println!("The value of x is: {}", x);
    x = 6;
    println!("The value of x is: {}", x);
}
```

</details>

### Immutabili e Constanti


In rust le **constanti** devono avere un valore già definto alla copilazione e possono essere create tramite la keyword `const` al posto di  `let`.

es:

```rust
const THREE_HOURS_IN_SECONDS: u32 = 60 * 60 * 3;
```

Mentre le variabili **immutabili** possono avere un valore definito anche a runtime.


### Shadowing

Può essere ridichiarata una variabile con lo stesso nome **anche di tipo diverso** nello stesso scope (la nuova variabile andrà a mascherare l'altra variabile che non sarà più accessibile).


```rust

    let spaces = "   ";
    let spaces = spaces.len();
```

## Type

### Integer 


| Length  | Signed  | Unsigned |
| ------- | ------- | -------- |
| 8-bit   | `i8`    | `u8`     |
| 16-bit  | `i16`   | `u16`    |
| 32-bit  | `i32`   | `u32`    |
| 64-bit  | `i64`   | `u64`    |
| 128-bit | `i128`  | `u128`   |
| arch    | `isize` | `usize`  |

`size` utilizza la word del processore su cui sta girando (64-bit computer sarà di 64 bit e su un architettura a 32 di 32).

| Number literals  |    Example    |
| ---------------- | ------------- |
| Decimal          | `98_222`      |
| Hex              | `0xff`        |
| Octal            | `0o77`        |
| Binary           | `0b1111_0000` |
| Byte (`u8` only) | `b'A'`        |

è possibile mettere uno `_` tra i numeri come separatore visuale

### Floating Point

possono essere `f64` o `f32` e la virgola è un punto `.`.

### Char

sono definite come un `valore Unicode Scalare`. (Non supportano solo l'ASCII) 

```rust
fn main() {
    let c = 'z';
    let z = 'ℤ';
    let heart_eyed_cat = '😻';
}
```

### Truple

> Truple sono di dimensione fissata e possono avere più tipi al loro interno.

Si possono accedere con il `.` e l'indice, e possono essere anche scomposte con il pattern matching.

```rust
fn main() {
    let tup: (i32, f64, u8) = (500, 6.4, 1);

    let (x, y, z) = tup;

    let five_hundred = tup.0;

    let six_point_four = tup.1;

    let one = tup.2;
}
```


### Array

Sono di dimensione fissata e tutti dello stesso tipo.

```rust
fn main() {
    // di tipo i32 5 elementi
    let a[i32;5] = [1, 2, 3, 4, 5];
    //un array di 5 elementi con valore di 3
    let a = [3; 5];
}
```

per accedere agli array si usano le `[index]`.


## Functions and expression

### Funzioni

si definiscono con la keyword `fn` per i parametri si come `nome:tipo,(altri parametri)` e il valore di ritorno si mette alla fine dei parametri dopo la parentesi con `-> tipo_di_ritorno`, si può omettere il `return`, infatti la funzione ritorna l'ultima espressione implicitamente.

esempio
```

fn five(x:i32) -> i32 {
    x*5
}

fn main() {
    let x = five(4);

    println!("The value of x is: {}", x);
}
```

### Statements and Expression


Gli **statements** sono instruzioni che non ritornano alcun valore (un esempio sono gli assegnamenti (in altri linguaggi tipo il c ritornano un valore in rust no)).

esempio:
```rust
fn main() {
    let y = 6;
    //è uno statments, quindi non si può avere un espressione come
    let x = (let y = 6);
}
```

Le **Expression** alla fine calcolano un dato di ritorno.

```rust
fn main() {
    let y = {
        let x = 3;
        x + 1
    };

    println!("The value of y is: {}", y);
}
```

## Control flow


## if-else

```rust
if espressione_booloneana {
    
}else if altra_espressione_booleana {
    
}else {
    
}

```
### Inline if

```rust
fn main() {
    let condition = true;
    // il tipo del valore di ritorno deve essere lo stesso
    // illegale: let number = if condition { 5 } else { "six" };
    let number = if condition { 5 } else { 6 };

    println!("The value of number is: {}", number);
}
```

### Loop

È un loop senza condizione infinito.
```rust 
//loop infinito
fn main() {
    loop {
        println!("again!");
    }
}
```
rust ha anche le keywords `continue` e `break` che possono essere usate anche con una label.

<details>
<summary>
esempio
</summary>

```rust
fn main() {
    let mut count = 0;
    'counting_up: loop {
        println!("count = {}", count);
        let mut remaining = 10;

        loop {
            println!("remaining = {}", remaining);
            if remaining == 9 {
                break;
            }
            if count == 2 {
                break 'counting_up;
            }
            remaining -= 1;
        }

        count += 1;
    }
    println!("End count = {}", count);
}
```

</details>

Si può anche fare il return di un valore da un loop con break (feature al quanto unica per quanto mi riguarda).

```rust
fn main() {
    let mut counter = 0;

    let result = loop {
        counter += 1;

        if counter == 10 {
            break counter * 2;
        }
    };

    println!("The result is {}", result);
}
```

### While

```rust
while boolean_expression{
    
}
}
```

### For

Serve per iterare su una collezione(esempio iterare su un array).

```rust
fn main() {
    let array = [10, 20, 30, 40, 50];

    for element in array {
        println!("the value is: {}", element);
    }
}
```

Inoltre può tornare utile con **Range** definito dalla standard library con cui si può definire su quanto iterare.

esempio
```rust
fn main() {
    for number in (1..4).rev() {
        println!("{}!", number);
    }
    println!("LIFTOFF!!!");
}
```
