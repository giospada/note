# Packages Modules Creates

> I **Creates** sono una o una libreria o un binario. 

> I **Packages** sono una o una create con un set di funzionalità (ogni packages continene un `Cargo.toml`), può contenere al massimo una libreria creates, ma quanti creates binari vuole

I creates fungono da `namespace`.

- `use` mette la path nello scope corrente
- `pub` fa diventare un item pubblic

- `mod` crea un altro modulo con il nome definito

```rust
mod front_of_house {
    mod hosting {
        fn add_to_waitlist() {}
        fn seat_at_table() {}
    }
    mod serving {
        fn take_order() {}
        fn serve_order() {}
        fn take_payment() {}
    }
}
```

<details>
<summary>
diventa
</summary>

```text
crate
 └── front_of_house
     ├── hosting
     │   ├── add_to_waitlist
     │   └── seat_at_table
     └── serving
         ├── take_order
         ├── serve_order
         └── take_payment
```
</details>

## Come riferirsi a degli oggetti del tree


- Le path assolute partono dal nome del `create`
- Le path relative partono da `self` (si riferisce a se stesso) e `super` (al modulo superiore)

si utilizza l'operatore `::` per navigare tra essi

<details>
<summary>
esempi
</summary>

```text
crate
 └── front_of_house
     ├── hosting
     │   ├── add_to_waitlist
     │   └── seat_at_table
     └── serving
         ├── take_order
         ├── serve_order
         └── take_payment
```
```rust
pub mod front_of_house{
// definizione di hosting e delle sue funzioni...
     pub mod serving{
        //definizione delle altre funzioni in serving
        pub fun funzione(){
            self::take_order();
            super::hosting::add_to_waitlist();
            create::front_of_house::serving::take_order();
        }
       
    }
}

```
</details>

## use keyword

`use` permette di prendere le path dentro lo scope.

<details>
<summary>
esempio
</summary>

```rust
mod front_of_house {
    pub mod hosting {
        pub fn add_to_waitlist() {}
    }
}

use self::front_of_house::hosting;
hosting::add_to_waitlist();

use self::front_of_house::hosting::add_to_waitlist;
add_to_waitlist();
```
</details>

### As

serve per rinominare un nome che importi

<details>
<summary>
es
</summary>

```rust
use std::fmt::Result;
use std::io::Result as IoResult;
fn function1() -> Result {
    // --snip--
    Ok(())
}
fn function2() -> IoResult<()> {
    // --snip--
    Ok(())
}
```

</details>

### pub use

oltre ad importarlo nello scope si può accedere anche dall'esterno.

### List with use

```rust
use std::io::Write;
use std::io;
```
si può scrivere come
```rust
use std::{io,io::Write};
//oppure
use std::io::{self,Write};
```

### Glob Operator

l'operatore `*` mette nello scope tutti gli item pubblici

```rust
use std::collections::*;
```

## Dividere in più File


