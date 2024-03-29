# Sintassi

ci serve per definire il linguaggio artificiale

## Definizione

- **sintassi**: è la descrizione dell'insieme di tutte le connotazioni alle quali associamo una denotazione
- **alfabeto**: è un insieme non vuoto di simbolo
- **stringa** su un alfabeto è una qualunque sequenza finita anche vuota, di simboli dell'alfabeto
- **linguaggio** su un alfabeto è un insieme di stringhe su un alfabeto
- **grammatica** è un qualunque formalismo (inieme di regole) che definisce un linguaggio

## Backus-Naur Form (BNF)

**BNF** è una notazione per descrivere le **grammatiche**; non tutti i linguaggi sono descrivibili tramite BNF .

Una BNF è una quadrupla (T,NT,X,P):
- T: è un alfabeto ovvero un insieme non vuoto di simboli detti **temrinali**
- NT è un insieme non vuoto di simboli detti **non terminali** distinti da quelli di T
- $X \in NT$ è il simobolo terminale non iniziale
- P è un insieme di coppie formate da:
    - un simbolo non terminale
    - un insieme di stringe di simboli terminali e non terminali (es (X,{$w_1,...w_2$}) si rappresenta $X ::= w_1|....|w_n$ (che si legge X è $w_1$ oppure ... $w_n$


<details>
<summary>
Esempio:
</summary>
 ({0, 1}, {X, Y}, X, {X ::= 0 | 0Y, Y ::= 1X})
</details>

Di solito di una BNF si indicano solamente le produzioni P:
- i **simboli non terminali** sono allora tutti quelli con cui iniziano le produzioni
- i **simboli terminali** sono tutti i simboli delle produzioni esclusi i non terminali
- il **simbolo iniziale** è il simbolo con cui inizia la prima produzione

<details>
<summary>
esempio
</summary>

({0,1},{X ,Y },X ,{X ::= 0 |0Y , Y ::= 1X }):  
X ::= 0 |0Y  
Y ::= 1X  
Non terminali: {X ,Y }; Simbolo iniziale: X ; Terminali: {0,1}.
</details>

**Un BNF si definisce:** La stringa $\omega$ di soli terminali appartiene al linguaggio sse
ottengo $\omega$ a partire da **X rimpiazzando ripetutamente ciascun
non terminale** con una delle stringhe alternative a lui associate
in una produzione.


Una **grammatica è ambigua** se si mostra che due modi diversi che una parola w appartiene al linguaggio.

<details>
<summary>
Esempio: 
</summary>

$F ::= x | y| F+F | F\times F$

$x + y\times x$ la posso ottenere in due modi diversi 
</details>

### Precedenze

per non rendere le nostre grammatiche non ambigue, usiamo delle estenzioni nell BNF:
1. fissiamo un ordinae di precedenza fra operatori distinti: $\times >+$ significa che $x+y\times x$ si legge $x+(y\times x)$ e non $(x+y) \times x$
2. fissiamo un' associatività perogni perazione
3. introduciamo l'uso delle parentesi

Consideriamo una BNF non ambigua.

Una stringa appartiene al linguaggio della BNF se è generata in modo unico.

Ovvero a ogni stringa del linguaggio resta naturale associa una struttura ricordiva.

L’AST ha un nodo per ogni espansione di simbolo. La radice corrisponde al simbolo iniziale e le foglie alle espansioni fatte con solo simboli terminali. I nodi figli di un nodo corrispondono ai non terminali contenuti nell’espansione del nodo padre

# Pseudo linguaggio funzinale puro non tipato

Sintassi della definizini di **funzini unarie**:
$f(w_1)=....corpo_1...$  
$...$  
$f(w_n)=....corpo_n...$  

- $f$ è il nome della funzione che stiamo definiendo 
- $w_i$ è una stringa sull’alfabeto formato da simboli terminali (costanti, costruttori) e da parametri formali (variabili)
- $corpo_i$  e un’espressione in pseudo-codice che puo utilizzare
    - parametri formali dell’i-esimo caso e tutte le costanti
    - espressioni if-then-else (sintassi C: . . .? . . . : . . .) 
    - chiamate di funzione della forma g(w) dove g e la funzione da chiamare e w e una stringa sull’alfabeto formato da simboli terminali e parametri formali di f

La funzione g(w) può essere:
- tutte quelle ovviamente implementabili e non interessanti ai fini dell’esercizio (operatori +, =,...)
- tutte quelle definite precedentemente nell’esercizio
- la f puo invocare la stessa f (chiamata ricorsiva); in tal caso la f si dice funzione ricorsiva


Sia $p$ una strina di terminali e $\omega$ una stringa di terminali e non terminali (variabili).


TODO:finisci slide 18/19


<details>

<summary>
es
</summary>

**es**

- $\{\langle\text{,",",}\rangle\}$ costruttori di coppie
- $\{::\}$ costruttore che separa la testa e la coda
- $\{[]\}$ rappresenta la lista vuota
- $\perp$ errore 

TODO: compleatre
</details>




## Turing-completezza

Se non ci restringessimo alla ricorsione strutturale (vedi dopo), qualunque programma esprimibile in un qualunque linguaggio di programmazione sarebbe esprimibile in questo pseudo-codice!


## Ricorsione Strutturale

Le **BNF** imprimono alle stringhe una **struttura ricorsiva**; In una struttura ricorsiva, un elemento o è atomico, o è composto a partire da parti più piccole con la stessa struttura; quindi:
- nei casi **atomici** il problema è semplice e si risove direttamente
- nei casi **composti**, si risolve prima il problema sulle componeti, ottenute le risposte si sintetizza larisposte, si sintetizza la risposta per il caso composto senza osservare più componenti $\implies$ uniformità della soluzione


Una funzione $f(\omega)$ dove $\omega$ è una stringa (formula) è definita per
ricorsione strutturale sse:
1. $f$ considera tutte le possibili produzioni che definiscono $\omega$ una e una volta sola
2. per ogni produzione f si richiama ricorsivamente solamente sulle sottoformule immediate di $\omega$


### Convergenza Ricorsione Strutturale

**Teorema:** tutte le funzioni definite per ricorsione strutturale
convergono su ogni input.  

**Dimostrazione:** a ogni chiamata ricorsiva, il numero di espansioni di non terminali necessarie per ottenere la stringa in input cala di 1 e, prima o poi, arriva a 0

## Induzione Strutturale

Sia P una proprietà che vogliamo dimostrare valere su tutte le stringhe $\omega$ di linguaggio generato da una BFN. La dimostraizone può essere data in questo modo:
1. Una sotto-dimostrazione per ogni produzione che genra $\omega$
2. In ogni sotto-dimostrazione possiamo assumere che P già valga su tutte le sotto-formule immediate di $\omega$