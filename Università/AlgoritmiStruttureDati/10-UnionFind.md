# UnionFind

> È una struttura dati che mantiene degli insiemi disgiunti, permette di sapere se due elemente sono disgiunti e di unirli nello stesso set


**Operazioni**
- `union`:  unisce due set disgiunti 
- `find`: trova il set di un elemento


## Implementazioni

### Quick Find

Per implementare il quick find si utilizza memorizza tutto in un albero di altezza 1, per fare ciò si diminuisce il costo di find a $O(1)$ ma il costo di union va a $O(n)$ nel caso peggiore

**euristica size**:
memorizza in ogni nodo la size del sottoalbero e quando deve fare l'union aggiunge gli elementi dell'albero più piccolo



### Quick Union

Per implementare il quick union l'albero non viene riaggiustato, quindi nel caso peggiore crea un albero che è una lista quindi abbiamo il costo peggiore del find in $O(n)$ e quello di union $O(1)$

**euristica rank**:
questa euristica mantiene un array dove ogni nodo mette anche la lunghezza la size del subtree
