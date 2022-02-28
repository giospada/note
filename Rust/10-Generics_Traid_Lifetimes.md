# Generics Traid Lifetimes

## Genircs

Servono per evitare le duplicazioni di codice, questa generalizzazione permette di definire strutture, enum , funzioni e implementazioni che hanno un tipo generico o che implementa alcuni traids.

### Funzioni

Per dichiarare il tipo generi in una funzione vanno dichiarati tra il nome di essa e i parametri

```rust
fn largest<T>(list: &[T]) -> T ;
```

### Strutture

I tipi generici vanno dichiarati dopo il nome della struttura.

```rust
struct Point<T> {
    x: T,
    y: T,
}

fn main() {
    let integer = Point { x: 5, y: 10 };
    let float = Point { x: 1.0, y: 4.0 };
}
```

### Emum

Analogamente alle strutture vanno definite dopo il nome.
```rust
enum Result<T, E> {
    Ok(T),
    Err(E),
}
```

### Metodi

Per i metodi vanno dichiarate quelle che si ereditano dalla struttura dopo `impl`

```rust
struct Point<T> {
    x: T,
    y: T,
}

impl<T> Point<T> {
    fn x(&self) -> &T {
        &self.x
    }
}

fn main() {
    let p = Point { x: 5, y: 10 };

    println!("p.x = {}", p.x());
}
```

dichiarando prima in `impl` rust capisce che il tipo è generico al posto di essere un istanza di un tipo reale come nell'esempio sotto.

```rust
impl Point<f32> {
    fn distance_from_origin(&self) -> f32 {
        (self.x.powi(2) + self.y.powi(2)).sqrt()
    }
}
```


## Trait

Servono per definire dei comportamenti che sono condivisi da più tipi.

Per creare un trait si usa la parola chiave `trait` seguita dal nome

```rust
pub trait Summary {
    fn summarize(&self) -> String;
}
```

Per implementare un trait in un tipo si usa la parla chiave `for` es:

```rust
pub trait Summary {
    fn summarize(&self) -> String;
}

pub struct NewsArticle {
    pub headline: String,
    pub location: String,
    pub author: String,
    pub content: String,
}

impl Summary for NewsArticle {
    fn summarize(&self) -> String {
        format!("{}, by {} ({})", self.headline, self.author, self.location)
    }
}

pub struct Tweet {
    pub username: String,
    pub content: String,
    pub reply: bool,
    pub retweet: bool,
}

impl Summary for Tweet {
    fn summarize(&self) -> String {
        format!("{}: {}", self.username, self.content)
    }
}
```

Possiamo creare trait se almeno o il trait o il tipo è all'interno del crate, non possiamo definirli su due tipi esterni dal trait



### trait come parametri

Si possono mettere come parametri per indicare che la funzione prende uno qualsiasi dei tipi che implementano quel determinato trait.

```rust
pub fn notify(item: &impl Summary) {
    println!("Breaking news! {}", item.summarize());
}
```

o anche, con i generic 

```rust
pub fn notify<T: Summary>(item: &T) {
    println!("Breaking news! {}", item.summarize());
}
```

Per indicare che il tipo preso in input deve implementare più trait si usa l'operatore `+`,

```rust
pub fn notify(item: &(impl Summary + Display));
pub fn notify<T:Summary+Display>(item: &T);
```

Si può rendere la signature della funzione più chiara utilizzando la keyword `where`

```rust
fn some_function<T, U>(t: &T, u: &U) -> i32
    where T: Display + Clone,
          U: Clone + Debug
          {}
```


Si può anche implementare un una funzione per ogni tipo che soddisfa un trait

```rust

impl<T: Display> ToString for T {
    // --snip--
}
```
