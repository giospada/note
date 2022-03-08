# Strutture Dati Basi

## Struttura Dati

**Def:** Definisce come i dati sono logicamente organizzati
Definisce le operazioni per accedere e modificare i dati

**Prototipi**: (descrizione ad alto livello della struttura)

**Implementazione**:(realizzazione concreta della struttura dati in un linguaggio di programmazione, determina i tempi d'esecuzione)

**Tipi di Strutture di dati**:
- Lineari: dati in ordine sequenziale
- Non-Lineari: nessun ordine

- Statiche: numero di elementi costante
- Dinamiche: numero di elementi può variare

- Omogenee: un solo tipo di dato memorizzabile 
- Eterogenee: differenti tipi di dato memorizzabili


## Dizionario / Array associativo

**Descrizione**:Contiene delle chiavi univoche, ognuna delle quali è associata ad un valore e ogni chiave è univoca

**Operazioni**:
- `search(key)`: cerca l'oggetto associato alla chiave
- `insert(key,dato)`: inserisce nel dizionario il dato associato alla chiave
- `delete(key)` elimina la coppia chiave e dato dal dizionario


## esempio di implementazini

**implementazione con array:** teniamo un array ordinato con tutte le chiavi

- `search(key)`: utilizziamo la ricerca binaria per trovare l'oggetto $O(\lg n)$
- `insert(key,dato)`: ricerchiamo la chiave più vicina e poi spostiamo tutte le chiavi di un passo più avanti $O(\lg n)+O(n)=O(n)$
- `delete(key)`: ricerchiamo la chiave spostiamo tutte le chiavi di un passo indietro $O(\lg n)+O(n)=O(n)$



**implementazione con liste**
- `search(Key k)`
    -  Ricerca sequenziale su lista non ordinata
    - Costo nel caso pessimo: $O(n)$
- `insert(Key k, Data d)`
    - Inserimento in testa alla lista
    - Costo nel caso pessimo: $O(1)$
- `delete(Key k)`
    - Ricerca sequenziale + rimozione
    - Costo nel caso pessimo: $O(n) + O(1) = O(n)$


## Linked List

**Descrizione** le linked list sono dove ogni elemento mantiene il pointer dell'elemento successivo, e mantiene lìordine sequenziale

![](vx_images/130594698826101.png)

**Operazioni**:
- Ricerca $O(n)$
- Inserimento $O(1)$
- Rimozione $O(n)$

## Stack

**Descrizione**: è una struttura dati che tiene gli elementi come una pila si può accedere solo all'ultimo elemento inserito ed eliminarlo

**Operazioni**:
- `push(elemento)`: aggiunge un nuovo elemento all'inizio della struttura $O(1)$
- `pop()`: rimuove l'elemento aggiunto più di recente alla struttura $O(1)$
<details>
<summary>
implementazione con le linked list vs array
</summary>

TODO:analisi ammortizzata da pag 34 [pdf](https://virtuale.unibo.it/pluginfile.php/1113427/mod_resource/content/4/04%20-%20Strutture%20dati%20elementari.pdf)

</details>

## Queue

**Descrizione**: è una SD che permette di aggiungere elementi alla fine e toglierne all'inizio, fa accedere all'primo e all'ultimo elemento


**Operazioni**:
- `queue(elemento)`: inseriesce l'elemento alla fine $O(1)$
- `dequeue()`: elimina l'elememto all'inizio $O(1)$


## Albero

**Def**: è un grafo con $n$ vertici e $n-1$ archi, in particolare c'è un unico percorso tra due vertici


## Albero Binario

**Def**: è un albero in cui ogni vertice ha massimo due figli è massimo un padre

**definizioni**:
- **profondità**:di un nodo u è la lungezza del percorso per arrivare ala radice
- **livello**: è l'insieme di nodi con la stessa profondità
- **altezza**: è la massima profondità dell'albero
- **grado**: è il numero dei suoi figli

**visita di profondità** (dfs)
- **in-order**:visita il nodo sinsitro, poi se stesso e poi il destro
- **post-order**: visita il destro,poi il corrente e poi il sinistro
- **pre-order**:visita il nodo corrente, poi il sinistro e poi il destro
