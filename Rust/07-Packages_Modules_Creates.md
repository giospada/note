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

## Referring to items in module tree




