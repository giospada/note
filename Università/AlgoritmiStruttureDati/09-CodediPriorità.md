# Code Priorità


## D Heap

> la d heap è una heap non binaria infatti ogni nodo ha d figli


**Operazioni**
- `findMin() → elem` Restituisce un elemento associato alla chiave minima
- `insert(elem e, chiave k)` Inserisce un nuovo elemento e con associata la chiave k
- `delete(elem e)` Rimuove un elemento dalla coda (si assume di avere accesso diretto a tale elemento e)
- `deleteMin()` Rimuove un elemento associato alla chiave minima
- `increaseKey(elem e, chiave d)` Incrementa la chiave dell'elemento e della quantità d (si assume di avere accesso diretto a tale elemento e)
- `decreaseKey(elem e, chiave d)` Decrementa la chiave dell'elemento e della quantità d (si assume di avere accesso diretto a tale elemento e)


### Implementazione

Implementazione con array, dal nodo i si può navigare:
- **l'ultimo figlio** è in posizione $(i*d)+1$
- **il primo figlio** è in posizione $((i-1)*d)+2$
- **il padre** è in posizione $\lceil (i-1)/d\rceil$





