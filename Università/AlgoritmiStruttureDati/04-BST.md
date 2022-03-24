
# Binary Search Tree

Il bst è una struttura dati che permette la ricerca di una chiave dentro l'albero


- `search(Key k)`: cerca l’oggetto associato alla chiave k
- `insert(Key k, Data d)`: aggiunge la coppia (k, d) al Dizionario
- `delete(Key k)`: elmina la coppia (k, d) dal Dizionario

**proprietà**: tutte le chiavi nel sottoalbero sinistro di v sono ≤ v.key e tutte le chiavi nel sottoalbero destro di v sono ≥ v.key


## Implementazione

`search`: confronta la chiave con quella del nodo corrente se è uguale ritorna il valore se è maggiore va ricorsivamente nel sottoalbero destro se è minore nel sinistro(Costo $O(h)$ dove h è l'altezza dell'albero)


`min` e `max`: min va nel nodo più a sinistra del'albero che riesce a trovare , il massimo nel nodo più a destra


`predecessore` il predecessore di un nodo è l'elemento che ha come valore il più vicino rispetto (algoritmo se esiste il nodo a sinistra si chiama `max` sul nodo di sinsitra il risultato è il predecessore, se non esiste prende il nodo padre se  è figlio sinistro se non lo è ritorna il parent)


`insert` incomincia dalla root e in base alla chiave che deve inserire se è maggiore del nodo a sinistra va in quello a destra se no va in quello a sinistra e ripete ricorsivamente questo procedimento finchè non trova un nodo nullo


`rimozione`: abbiamo tre casi:
- il nodo è una foglia lo rimuoviamo direttamente
- il nodo ha un figlio,  mettiamo il figlio al poso del padre
- il nodo ha entrabi i figli prendiamo il massimo nel sottoalbero sinistro

