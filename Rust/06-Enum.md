# Enum

Sono strutture il quale valore può essere solo uno di quelli definiti nella dichiarazione.

Es:
```rust
enum IpAddrKind {
    V4,
    V6,
}

fn main() {
// si può accedere ai valori tramite `::`
    let four = IpAddrKind::V4;
    route(IpAddrKind::V6);
}

fn route(ip_kind: IpAddrKind) {}

```

Il valore può anche contenere dati:

```rust
fn main() {
    enum IpAddr {
        V4(u8, u8, u8, u8),
        V6(String),
    }
    let home = IpAddr::V4(127, 0, 0, 1);
    let loopback = IpAddr::V6(String::from("::1"));
}
```

Si usare tutti i tipi persino le strutture (inline e non).

<details>
<summary>
es
</summary>

```rust
enum Message {
    Quit,
    Move { x: i32, y: i32 },
    Write(String),
    ChangeColor(i32, i32, i32),
}

fn main() {}
```

</details>

E si possono implementare metodi con il costrutto `imp` esattamente come sulle strutture.


## Match

Il match deve avere come braccio tutti i valori possibili per farlo si può utilizzare una variabile che prende i casi che non sono stati definiti nel match.


```rust
#[derive(Debug)]
enum UsState { Alabama, Alaska,}
enum Coin {  Penny,  Nickel,  Dime,  Quarter(UsState), }

fn value_in_cents(coin: Coin) -> u8 {
 match coin {
        Coin::Penny => 1,
        Coin::Nickel => 5,
        Coin::Dime => 10,
        Coin::Quarter(state) => {
            println!("State quarter from {:?}!", state);
            25
        }
    }
}
fn main() {  value_in_cents(Coin::Quarter(UsState::Alaska)); } 
```

Come già accennato nel match per renderlo completo di tutti i casi si può utilizzare una variabile "catch-all" o `_` vome segnaposto 

```rust
//catch-all
fn main() {     let dice_roll = 9;
    match dice_roll {
        3 => add_fancy_hat(),
        7 => remove_fancy_hat(),
        other => move_player(other),
    }

    fn add_fancy_hat() {}
    fn remove_fancy_hat() {}
    fn move_player(num_spaces: u8) {}
} 
//segnaposto
fn main() {     let dice_roll = 9;
    match dice_roll {
        3 => add_fancy_hat(),
        7 => remove_fancy_hat(),
        _ => reroll(),
    }

    fn add_fancy_hat() {}
    fn remove_fancy_hat() {}
    fn reroll() {}
} 
```
### Option

Option è una delle strutture più usate e riesce ad esprimere il concetto di null senza però avere i problemi che hanno gli altri linguaggi (Come il NullPointerException).

```rust
fn main() {
     fn plus_one(x: Option<i32>) -> Option<i32> {
        match x {
            None => None,
            Some(i) => Some(i + 1),
        }
    }

    let five = Some(5);
    let six = plus_one(five);
    let none = plus_one(None);
}
```


