# Struct

Strutture come le truprle possono contenere tipi di dato diversi, ma ogni campo è associato ad un nome.
```rust
struct User {
    active: bool,
    username: String,
    email: String,
    sign_in_count: u64,
}

fn main() {
    let user1 = User {
        email: String::from("someone@example.com"),
        username: String::from("someusername123"),
        active: true,
        sign_in_count: 1,
    };
}

```

## Struct Truple 

Servono in pratica per dare un nome alle truple.

```rust
struct User {
    active: bool,
    username: String,
    email: String,
    sign_in_count: u64,
}

fn main() {
    let user1 = User {
        email: String::from("someone@example.com"),
        username: String::from("someusername123"),
        active: true,
        sign_in_count: 1,
    };
}
```

## Unit Structs

Sono strutture senza dati, che serviranno specialmente per l'uso dei traid.

```rust
fn main() {
    struct AlwaysEqual;

    let subject = AlwaysEqual;
}
```

## Display Struct e Debug

Per scrivere in output una struttura basta farla Fargli derivare la Debug traids e al posto del `{}` nel `println!` usare `{:?}`.

```rust
#[derive(Debug)]
struct Rectangle {
    width: u32,
    height: u32,
}

fn main() {
    let rect1 = Rectangle {
        width: 30,
        height: 50,
    };

    println!("rect1 is {:?}", rect1);
}
```

Oltre a `println!`, un altra macro molto utilizzata è `dbg!` permette di scrivere sia l'operazione che il risultato (e ritorna l'ownership).

```rust
#[derive(Debug)]
struct Rectangle {
    width: u32,
    height: u32,
}

fn main() {
    let scale = 2;
    let rect1 = Rectangle {
    // ouput :[src/main.rs:10] 30 * scale = 60
        width: dbg!(30 * scale),
        height: 50,
    };
    //output [src/main.rs:14] &rect1 = Rectangle {
        //width: 60,
        //height: 50,
    //}
    dbg!(&rect1);
}
```

## Metodi

I metodi sono come le funzioni ma definiti dentro un contesto di una struct e quindi il loro primo parametro è sempre `self` (che rappresenta l'instanza della struttura su cui il metodo è stato chiamato)

I metodi devono essere implementati tramite la stuttura `impl` (dentro il constutto impl si può usare `Self` come alias alla struct sulla quale stiamo facendo l'impl ).

```rust
struct Rectangle {
    width: u32,
    height: u32,
}

impl Rectangle {
    fn increment_height(&mut self){
        height=height+1;
    }
    fn area(&self) -> u32 {
        self.width * self.height
    }
}

fn main() {
    let rect1 = Rectangle {
        width: 30,
        height: 50,
    };
    println!(
        "The area of the rectangle is {}",
        rect1.area()
    );
}
```

> NOTE
> in rust non c'è il `->` operator perchè rust riesce a fare il dereferencing automaticamente in base al tipo che stai utilizzando


## Funzioni Associate

Si possono creare metodi che non prendono `self` in input, molte volte sono utilizzate come costruttori, e si può accedere ad esse attraverso l'operatore `::`.