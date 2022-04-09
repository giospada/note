# CompetitiveProgramming

KISS: "Keep It Short and Sample"

## Complete search

tips:
- programmi che filtrano vs quelli che generano
    - quelli che filtrano sono di solito interativi e scelgono le soluzioni corrette di solito interativi
    - quelli che generano invece gerano step by step la soluzione ricorsivamente
- cercare i casi in cui la soluzione parziale si capisce che non arriverà mai a una totale
- cercare le simmetrie
- pre computare dei valori o precalcolarli

## Sorting e Searching

il sorting degli array in input molte volte può semplificare la risoluzione del problema ( molte volte è utilizzato qanod ci sono i Shuldering Events o Task)
Il searching è utilizzato soprattutto con la binary search non si puo solo cercare un valore in un array ordinato ma anche provare per a vedere il massimo in cui una funzione diventa vera 

## Dynamic Programming 

la programmazione dinamica può essere di due tipi principalmente 
- bottom-up: questa solitamente genera in una tabella (kanapsak)
- top-down: di solito è una memorizzazione di un backtraking (fibonacci)


## Grafi

i grafi sono coposti da vertici V(n) e i collegamenti E(m)
rappresentazione : pre rappresentare i grafi si può usare:
- Adjacency Matrix: una griglia che per V*V con per due vertice k j in grind\[k][j]=la distanza tra k e j $O(V^2)$
- Adjacency List: solitamente un vettore di vettori contiene per ogni vertice k i vertici toccanti k $O(V+E)$
- Edge List: una vector di pair contenete per ogni collegamento i due vertici $O(E)$

(il grado di un vertice è il numero di collegamenti)

### Tipi di Grafi

- directed Graph: è un grafo in cui i collegamenti hanno direzioni
- undirected Graph: è un grafo in cui i collegamenti non hanno direzioni
- weighted Graph: è un grafo in cui i colegamenti hanno un costo 
- directed Acyclic Graph(DAG): sono gradi con direzini senza cicli
- successor Graph (SG):è un tipo speciale di DAG doveogni nodo ha solo un nodo di uscita

- il ciclo di eulero si ha quando tutti i vertici hanno grado pari
- il percoso di eulero si ha quando tutti i vertici tranne 0 o due hanno grado pari ( incomincerà sempre da uno di grado dispari per finire nell'altro di grado dispari)


### Algoritmi sui Grafi

#### esplorazione

**DFS**(Deep first search/Ricerca in profondità)
**BFS**(Breadth first search/Ricerca in ampiezza)
costo :$O(n+m)$
possono essere usati per:
- verificare la connettivià
- trovare cicli
- trovare se si può colorare con due colori 


#### ricerca cammino minimo

**Bellman-Ford**:per ogni nodo meno uno ricalcola la distanza di ogni collegamento 
costo: $O(nm)$
- può essere usato anche per la ricerca di cicli negativi:(basta riusare lo stesso algoritmo e vedere se il 
costo di un nodo diminuiscae)   
**Dijkstra**:ogni volta seleziona il nodo non visitato con distanza minore 
costo: $O(n+m \lg m)$
**Floyd-Warshall** :usa una adjansi matrix e per ogni nodo guarda prende tutte le coppie di nodi le somma e le aggiorna se è la minima distanza
costo $O(n^3)$

#### strani

**TypologicalSort(DAG)** :si usa un DFS e quando tutti i dipendenti sono stati inseriti nell'array viene iserito anche lui (l'array va revesato)
- si possono appicare varie tecniche di DP per rispondere a varie domande come
  - numero di percorsi tra due nodi
  - quanti percorsi esistono 
  - qual'e il numer minimo/massimo di nodi nella path
  - quali nodi sono presenri in ogni percorso

**FindingSuccessor(SG)**:si crea un array bidimensionale con il nodo e il quanti step avanti(si registrano solo le potenze di due) 
- si può trovare facilmente con $O(\log k)$ il nodo a k nodi di distanza da un nodo casuale

**Cycle Detection(SG)**:  sbloccare tutti i nodi e verificare se uno è già sbloccato
costo:$O(n)$ tempo e $O(n)$ memoria
- trova un ciclo
**Floud's Algorithm(SG)**:usa due puntatori che percorrono il grafo uno di due step l'altro di uno 
costo:$O(n)$ tempo e $O(1)$ memoria
- trova un ciclo

**Kruskal's Algorithm**:prima cosa si ordinano i collegamenti per peso poi si agguingono se non i nodi non sono nello stesso set finisce quando tutti i vertici sono dello stesso set(si usa Union-Find di solito come set)
costo: $O(m \log m)$

#### Cicli

- **SCC** :(strong connetted component)(Tarjan's algorithm) come prima cosa si fa un dfs dove si registrano i nodi all'uscita, poi si reversano tutti i collegamenti e si fa un dfs con i collegamenti reversati e partendo dall'ultimo nodo in uscita del primo dfs fino al primo nodo uscito, ogni volta che si incomincia una dfs tutti i nodi esplorati per la prima volta fanno parte del ciclo

## Alberi

gli alberi hanno n vertivi e n-1 collegamenti (aggungere un collegamento crea un ciclo, toglerne uno separa l'albero in due)

**attraversare un albero**: si può usare un dfs in cui non si tiene i nodi già visitati ma basta non riesplorare quello appena visistato

*Lowest Common Ascensor*: il migliore algoritmo e usare l'esplorazione euleriana cioè pushare nell array ogni volta che il nodo viene usato nel dfs sia quando viene attravaersato sia quando chiama un altro figlio e quando esce con questo si puo salvare un arrey con la depth del nodo a quel punto e facile trovare il lca semplicemente trovando due indice che contengono i due nodi e trovare il minimo nel array dell depth compreso tra quei indici (con un sparce table o un binary tree si puo velocizzare la ricerca)




## Complessità computazionale

circa un compiuter fa 100M ( 1M=1'000'000 ) in pochi secondi quindi calcola.
- k loop innestati onguno per n vlote $O(n^k)$
- na ricorsione a L livelli con b chiamate $O(b^l)$
- Dp dopo

| n           | Worst AC Algorithm                  |
| :---------- | :---------------------------------- |
| ≤ [10..11]  | $O(n!), O(n^6 )$                    |
| ≤ [15..18]  | $O(2^n × n^2 )$                     |
| ≤ [18..22]  | $O(2^n × n)$                        |
| ≤ 100       | $O(n^4 )$                           |
| ≤ 400       | $O(n^3 )$                           |
| ≤ 2K        | $O(n^2 lg n)$                       |
| ≤ 10K       | $O(n^2 )$                           |
| ≤ 1M        | $O(n lg n)$                         |
| ≤ 100M      | $O(n), O(lg n), O(1)$               |


## Strutture Dati

- staic array :di solito l'ampiezza è inizializzata con il massimo di laghezza dell'input  
- vector :(è come gli static array ) ma può essere ridimensionato a runtime 
- bitset :è come un array di booleani che occupa meno spazio e le bit operation
- stack: LIFO push and pop in $O(1)$ accesso al top()
- queue: FIFO push and pop in $O(1)$ accesso al top() e end()
- deque: è come un vector con push e pop sia dietro che davanti (back() e front )
- set: serve per vedere se un valore è inserito $O(log n)$ e si piuò scorrere già ordinato
- map : è come il set ma usa gli hash $O(1)$
- priority_queue : push e fa il pop dell'elemento maggiore $O(log n)$
- union-find: è una struttura che permette di sapere se due ementi appartangono allo stesso set
    - Implementazione: si crea un array nel quale iniziamlente ogni nodo punta a se stesso poi ogni volta che si unisce se non sono nello stesso set si cambia un root con il valore dell'altro(con la pathcompression ogni volta che si cerca in un nodo che non punta al root si aggorna con il valore del root)
- 

## Funzioni/Librerie Belle

#### lib <bits/stdc++.h> 

libreria che include tutte le librerie standard

####  lib <algorithm>

- [void sort (RandomAccessIterator first,RandomAccessIterator last, Compare comp)](https://www.cplusplus.com/reference/algorithm/sort/): riordina nel range first e last in per grandezza se non si specifica una funzione comp

####  lib <math.h>

- [float hypot(float x, float y)](https://www.cplusplus.com/reference/cmath/hypot): ipotenusa di un triangolo rettangolo $\sqrt(x^2 + y^2)$



