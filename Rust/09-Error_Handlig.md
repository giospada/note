# Error_Handlig


## Painc

è una macro che stoppa fa l'abort del programma con una messaggio d'errore e stampando il back trace

## Result

Molti errori possono essere gestiti dal programma, e per farlo si utilizza la enum Result definita:

```rust
enum Result<T,E>{
    Ok(T),
    Err(E),
}
```

esempio di utilizzo

```rust
use std::fs::File;

fn main() {
    let f = File::open("hello.txt");

    let f = match f {
        Ok(file) => file,
        Err(error) => panic!("Problem opening the file: {:?}", error),
    };
}
```

### Metodi

- `unwrap` **metodo** che ritorna il risultato e se si verifica l'erre manda in panic il programma
- `expect` **metodo** uguale a unwrap ma puoi aggiungerci un messaggio d'errore
- `unwrap_or_else`  **metodo** che prende una lambda che viene eseguita in caso d'errore


### Funzioni che ritornano un Result


per le funzioni che ritornano un result possoamo utilizzare l'operatore `?` al termine della chiamata di funzione che ritorna un result, in modo che se ci sia un errore venga direttamente fatto il return di quell'errore

<details>
<summary>
esempio in cui si capirà sicuramente meglio
</summary>

```rust

#![allow(unused)]
fn main() {
use std::fs::File;
use std::io::{self, Read};

fn read_username_from_file() -> Result<String, io::Error> {
    let f = File::open("hello.txt");

    let mut f = match f {
        Ok(file) => file,
        Err(e) => return Err(e),
    };

    let mut s = String::new();

    match f.read_to_string(&mut s) {
        Ok(_) => Ok(s),
        Err(e) => Err(e),
    }
}
}
```

si può trasformare in  

```rust


#![allow(unused)]
fn main() {
use std::fs::File;
use std::io;
use std::io::Read;

fn read_username_from_file() -> Result<String, io::Error> {
    let mut f = File::open("hello.txt")?;
    let mut s = String::new();
    f.read_to_string(&mut s)?;
    Ok(s)
}
}
```

</details>
 
È importante che il return della funzione sia compatibile 