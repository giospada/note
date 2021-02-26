---
tags: [Computer]
title: Cyber challange
---


# CyberChallange

## PreTest

**strlen** ritorna la lunghezza della string fino al carattere nullo

**sizeof** 

> quando si assegna una strina ad un array di char non bisogna
> mettere il carattere '\0' perchè tutti i valori sono 
> inizializati a zero

priorità degli operatori

| priorità | opratoroe    | descrizione                                       | altro                                  |
| -----    | -----        | -----                                             | -----                                  |
| 1        | ++ --        | Suffix/postfix increment and decrement            | Left-to-right                          |
|          | ()           | Function call                                     |                                        |
|          | []           | Array subscripting                                |                                        |
|          | .            | Structure and union member access                 |                                        |
|          | ->           | Structure and union member access through pointer |                                        |
|          | (type){list} | Compound literal(C99)                             |                                        |
| 2        | ++ --        | Prefix increment and decrement[note 1]            | Right-to-left                          |
|          | + -          | Unary plus and minus                              |                                        |
|          | ! ~          | Logical NOT and bitwise NOT                       |                                        |
|          | (type)       | Cast                                              |                                        |
|          | *            | Indirection (dereference)                         |                                        |
|          | &            | Address-of                                        |                                        |
|          | sizeof       | Size-of[note 2]                                   |                                        |
|          | _Alignof     | Alignment requirement(C11)                        |                                        |
| 3        | * / %        | Multiplication, division, and remainder           | Left-to-right                          |
| 4        | + -          | Addition and subtraction                          |                                        |
| 5        | << >>        | Bitwise left shift and right shift                |                                        |
| 6        | < <=         | For relational operators < and ≤ respectively     |                                        |
|          | > >=         | For relational operators > and ≥ respectively     |                                        |
| 7        | == !=        | For relational = and ≠ respectively               |                                        |
| 8        | &            | Bitwise AND                                       |                                        |
| 9        | ^            | Bitwise XOR (exclusive or)                        |                                        |
| 10       | \            |                                                   | Bitwise OR (inclusive or)              |
| 11       | &&           | Logical AND                                       |                                        |
| 12       | \            | \                                                 |                                        |
| 13       | ?:           | Ternary conditional[note 3]                       | Right-to-left                          |
| 14       | =            | Simple assignment                                 |                                        |
|          | += -=        | Assignment by sum and difference                  |                                        |
|          | *= /= %=     | Assignment by product, quotient, and remainder    |                                        |
|          | <<= >>=      | Assignment by bitwise left shift and right shift  |                                        |
|          | &= ^= \      | =                                                 | Assignment by bitwise AND, XOR, and OR |
| 15       | ,            | Comma                                             | Left-to-right                          |


