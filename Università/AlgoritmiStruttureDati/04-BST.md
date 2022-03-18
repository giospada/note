
# Binary Search Tree

Il bst è una struttura dati che permette la ricerca di una chiave dentro l'albero


- `search(Key k)`: cerca l’oggetto associato alla chiave k
- `insert(Key k, Data d)`: aggiunge la coppia (k, d) al Dizionario
- `delete(Key k)`: elmina la coppia (k, d) dal Dizionario

**proprietà**: tutte le chiavi nel sottoalbero sinistro di v sono ≤ v.key e tutte le chiavi nel sottoalbero destro di v sono ≥ v.key


## Implementazione

`search`: confronta la chiave con quella del nodo corrente se è uguale ritorna il valore se è maggiore va ricorsivamente nel sottoalbero destro se è minore nel sinistro(Costo $O(h)$ dove h è l'altezza dell'albero)


`min` e `max`: min va nel nodo più a sinistra del'albero che riesce a trovare , il massimo nel nodo più a destra