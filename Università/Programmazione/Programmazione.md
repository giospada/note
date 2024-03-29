# Programmazione

> 20/09/2021


## Argomenti 

- le principali tecniche
- gli strumenti più importanti di c++


## Modalità d'esame

- scritto max 24
- orale (descrizione del progetto)


## come studiare all'università

- venire a lezione preparati
- fai le domande quando qualcosa non capisce 
- non studiare dalle slide
- scegliere un libro su cui studiare

## Lezione 1 (21/09/2021)

> un `sistema di calcolo` è formato da hardware e software (collezione di programmi che i calcolatori eseguono)

l'hardware (il calcolatore) ha 5 componenti principali:
- dispositivi di input
- dispositivi di output
- processore
- memoria principale (RAM)
- memoria secondaria (dove vengono memorizzati i dati in modo permanente)

### Memoria Principale

> la memoria principale è una sequenza di locazioni che si possono accedere attraverso gli indirizzi (ogni indirizzo contiene 8 bits, un byte)

Quando si hanno dati che contengono più byte si utilizza l'indirizzo del primo byte

nella memoria i dati vengono immagazzinati tutti come byte(il valore 'A' e 65 in byte hanno lo stesso valore), il tipo viene definito dall'istruzione che sta eseguendo

i linguaggi ad alto livello ci risolvono questo tipo ti problemi


### CPU

> central process unit

la cpu esegue istruzioni assembly per esempio

```c++
__asm{
   mov loc1 loc2
   addi 32 28 R3
   mov eax,100
   leave
   ret
  };
```

questo codice è la traduzione del linguaggio macchina nel quale vengono sostituite le istruzioni con una serie di byte, è traducibile in assembly che fa parte dei linguaggi a basso livello

### Linguaggi ad alto livello

> sono linguaggi di programmazione che astraggono il linguaggio macchina e assomigliano di più ai linguaggi naturali (alla fine per essere eseguiti vengono tradotti in linguaggio macchina)


questi linguaggi ad alto livello hanno bisogno di:
- linker: collega le funzioni chiamate nel codice con le librerie 
- compilatore: traduce il codice ad alto livello ad un codice comprensibile dal computer

### Algoritmi e Programmi

- un algoritmo è una serie di istruzioni che risolve un certo problema, scritta in una forma logica qualsiasi
- un programma è un algoritmo espresso in un linguaggio di programmazione

Problem Solving e implemantazione

domande del problem solving:  
- quale è l'input?
- cosa contiene l'output?
- come sono organizzati l'input e l'output?

implementazione:  
- tradurre l'algoritmo
- compilare
- eseguire il codice
- rivelare errori nel nell'algoritmo


#### Diagrammi di flusso

tipi di nodi:  
- nodo comando: un rettangolo 
- nodo condizione: un rombo con scritta una condizione
- nodi speciali: di fine e di inizio

esempio visualizzabile con mermaid:

```mermaid
graph TD
B[nodo speciale di inizio: input m ]
B --> C{nodo condizione: <br>il resto  della  divisione <br>di m per  due è 0 }
C --> |falsa| D[blocco di fine:ouptut dispari]
C --> |vera| E[blocco di fine: output pari]
```

# C++


## Reference

i reference sono dei pointer immutabili, a differenza dei pointer non bisogna fare il dereferencing perchè il compilatore li tratta come se fossero l'oggetto stesso

> A reference can be thought of as a constant pointer (not to be confused with a pointer to a constant value!) with automatic indirection, ie the compiler will apply the * operator for you.



## Array

gli array statici possono essere passati solo per reference ma a differenza dei reference normali si scrive come `[]`

```c++

//l'array a non è una copia dell'array ar ma è lo stesso array passato per reference
void passarray(int a[]){
  return;
}
int main(){
  int ar[5]={0};
  passarray(ar);
}
```

### Array Multidimensionali

gli array multidimensionali quando sono passati ad una funzione dev'essere esplicitato il numero dell'ultime dimensioni perché il compilatore deve sapere dove incomincia il nuovo array

## Stringhe

Possiamo utilizzare le c string, cioè degli array di char il cuoi ultimo carattere è il terminale delle stringhe `'\0'`.

funzioni fatte:  
- strlen
- strcat
- strncpy
- strcmp
- atoi
- atol
- atof


## Struct

Vengono copiate per valore, e se contengono un array statico al loro interno anche esso viene copitato per valore.









