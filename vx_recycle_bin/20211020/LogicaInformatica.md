---
title: Logica
date: Settembre 2021
author: Giovanni Spadaccini
---

# Sintassi

ci serve per definire il linguaggio artificiale

## Definizione

- **sintassi**: è la descrizione dell'insieme di tutte le connotazioni alle quali associamo una denotazione
- **alfabeto**: è un insieme non vuoto di simbolo
- **stringa** su un alfabeto è una qualunque sequenza finita anche vuota, di simboli dell'alfabeto
- **linguaggio** su un alfabeto è un insieme di stringhe su un alfabeto
- **grammatica** è un qualunque formalismo (inieme di regole) che definisce un linguaggio

## Backus-Naur Form (BNF)

BNF è una notazione per descrivere le grammatiche; non tutti i linguaggi sono descrivibili tramite BNF (TODO: aggiungere nota).

Una BNF è una quadrupla (T,NT,X,P):
- T: è un alfabeto ovvero un insieme non vuoto di simboli detti temrinali
- NT è un insieme non vuoto di simboli detti non terminali distinti da quelli di T
- $X \in NT$ è il simobolo terminale non iniziale
- P è un insieme di coppie formate da:
    - un simbolo non terminale
    - un insieme di stringe di simboli terminali e non terminali (es (X,{$w_1,...w_2$}) si rappresenta $X ::= w_1|....|w_n$ (che si legge X è $w_1$ oppure ... $w_n$

: Esempio: ({0, 1}, {X, Y}, X, {X ::= 0 | 0Y, Y ::= 1X})


Di solito di una BNF si indicano solamente le produzioni P:
- i simboli non terminali sono allora tutti quelli con cui iniziano le produzioni
- i simboli terminali sono tutti i simboli delle produzioni esclusi i non terminali
- il simbolo iniziale è il simbolo con cui inizia la prima produzione

La stringa w di soli terminali appartiene al linguaggio sse
ottengo w a partire da X rimpiazzando ripetutamente ciascun
non terminale con una delle stringhe alternative a lui associate
in una produzione.


Una grammatica è ambigua se si mostra che due modi diversi che una parola w appartiene al linguaggio.

Esempio: 
$F ::= x | y| F+F | F\times F$

$x + y\times x$ la posso ottenere in due modi diversi 

### Precedenze

per non rendere le nostre grammatiche non ambigue, usiamo delle estenzioni nell BNF:
1. fissiamo un ordinae di precedenza fra operatori distinti: $\times >+$ significa che $x+y\times x$ si legge $x+(y\times x)$ e non $(x+y) \times x$
2. fissiamo un' associatività perogni perazione
3. introduciamo l'uso delle parentesi

Consideriamo una BNF non ambigua.

Una stringa appartiene al linguaggio della BNF se è generata in modo unico.

Ovvero a ogni stringa del linguaggio resta naturale associa una struttura ricordiva.

L’AST ha un nodo per ogni espansione di simbolo. La radice corrisponde al simbolo iniziale e le foglie alle espansioni fatte con solo simboli terminali. I nodi figli di un nodo corrispondono ai non terminali contenuti nell’espansione del nodo padre.




