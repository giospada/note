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



