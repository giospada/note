# Allenamento per i Nazionali 

## Parlare di Algoritmi

domande sugli algoritmi:
- cosa fa
- quanto bene lo fa
- lo fa davvero
 
(farlo in maniera matematicamente precisa)


**Cosa fa?**
intput:
- quali oggetti deve ricevere in input (segnatura)
- quali condizioni devono valre questi oggetti(precondizione)
output:
- quali oggetti deve produrre in output (segnatura)
- che prprietà hanno gli oggetti prodotti dall'algoritmo(postcondizione)

Es.
``` c++
// precondizioni: v deve essere ordinato
// e deve contenere e 

in riceca_binaria(const vector<int>& v,int e); //segntura

// postocondizione: posizione dell'elemento v

// precondizione v non è vuoto

void rimuovi_duplicati(vector<int>& v);//signatura

//postcondizione il valore finale di v è una sottosequnza
//in cui non sono presenti duplicati 
```

Serve per:
- comunicare il comportamento di una funzione (senza scrierle fomalemtne)
- debuggare il programma (susare assert)
- pre utilizzare correttamente la funziamento (senza scrierle fomalemtne)
- dimostrare la correttezza di un programma (non ci interessa)

**Quanto bene lo fa?**

confrontare gli algoritmi e la loro efficenza:
- tempo di esecuzione
- spazio di memoria occupato

la performance dell'algoritmo dipende:
- dagli input
- dalla macchina che lo esegue
- a fattori casuali

dipendenza dagli input;
- decidere i paramatri più rilevanti del l'input
- decidere quali input ci interessano di più (caso migliore, medio, peggiore)
- ottenere un informazione sintetica che non dipenda dal calcolatore

Proposta:
- ci focalizziamo su valori grandi
- ignorare i fattori moltiplicativi
- sistisuire funzioni colplesse con funzioni semplici

Complessita asintotica: O grande
f(n ) appartine a O(g(n)) se f non crese mai più di g 

TODO:ricopiare in matematicese dalle slide

caso medio:
- assegnamo un peso a degli input e facciamo la media pesata dei tempi e spazi (bad)
- se l'algoritmo ha un comportamento rando su cisacun input e facciamo la media dei tempi/spazi impiegati per un input (caso medio randomizzato)
- se l'algoritmo viene eseguito più volte in seqenza, facciamo la media della sequenza di esecuzione nel peggiore

**Se lo fa davvero?**
- ragionamento passo passo
- scomposizione in funzioni con pre e post condizioni
- asserzione che deve essere vera ad ogni interazione di un ciclo


## Induzione, ricorsione ed esponenziazione veloce

Problemi:

Esponenziale:  
dati $b$ e $n$ cacola $b^n$

Fibonacci:  
calcola l'$n$esimo numero Fibonacci $F_n$ dove:  
$F_0 = F_1 =1$  
$F_{n+1} = F_n + F_{n-1}$


Induzione:  
sia $X={x,y,z...}$ un insieme (finito o infinito) ma **parzialemente ordinato**(deve esistere un <)
- x<x non è mai vero
- x<y e y<z implica x<z
- non ci sono sequenze discendenti infinite: x>y>z>...
**Parzilmente**:puù essere che x non sia minore di y e nemmono y minore di x

Esempi:
- numeri interi 2<5
- stringe o tuple in maniera lessicografica "ciao"<"mondo", (2,4)<(4,2)
- Tuple con un ordine compoente per componente (1,1)<(4,2)
- insiemi con inclusione negli insiemi

Dimostrazione per l'induzione
Sia X insieme parzialmente prdinato P(x)

TODO: riprendere dalle slide

Soluzione rivorsiva:
riscriviamo la soluzione in matematica in un linguaggio di programmazione

## Algoritmi

### Ricerca

lineare:
scorro tutto l'arrei e guardo se c'è $O(n)$

binaria:
(se il vettore è ordinato)
si può spezzre l'array in range e guardare solo nel range in cui dovrebbe essere $O(log n)$

### Ordinamento

lenti $O(n^2)$:
- selection:
    - descrizione: metto nel posto giusto l'i 
       esimo elemento più piccolo in posizione i
- insertion sort:
    - descrionzione: vogliamo avere ogni volta un array sampre più grande sempre ordinato (partendo da un array di uno aggiungiamo tutti gli altri)
- bubble sort:
    - descrizione:ogni due elementi vicini che hanno ordine sbagliato li inverto 
    - funziona perchè una volta che ho l'elemento massimo del vettore che sto considerando arriva in fondo

Veloci $O(n log n)$:
- marge sort:lo dividiamo in due pezzi li ordiniamo e una volta ordinati li uniamo
- quick sort:prima separiamo il vettore in due parti e le ordino
- heap sort

Speciali $O(n)$:
- counting sort:si può usare quando A[i] sono in un insieme limitato, così mi limito a fare una passata di quante volte ci sono nel vettore gli elementi
- radix sort: con numeri potenzialmente più grandi (o stringe) ordino sempre per la cifra i più significativa

### Selezione

Array non ordinato di lunghezza N e un intero k e dobbiamo trovare il k esimo elemento

usare un quick select 


## Problemi

- https://volterra.olinfo.it/
- Problema 1: https://szkopul.edu.pl/problemset/problem/vvd6w7n7EXFVEg3nkqGxEirV/site/?key=statement
- Problema 2: https://szkopul.edu.pl/problemset/problem/xCiDtZ0ZX70fyac1Sav8d37J/site/?key=statement
- Problema 3: https://szkopul.edu.pl/problemset/problem/KkN5UonnNGIG3AuMqoI6xr62/site/?key=statement 
