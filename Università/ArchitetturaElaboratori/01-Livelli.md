

# Livelli

## Astrazione e Implementazione

Nell'informatica si usano i principi di astrazione e implementazione, per diminuire la complessità, l'astrazione grazie a delle interfaccia accede alle implementazione (che utilizzando l'astrazione non bisogna più sapere com'è costruita)

> astrazione: Si presenta la soluzione ad un problema concentrandosi solo su alcuni aspetti “rilevanti” (ad esempio, come ottenere la soluzione componendo soluzioni di problemi più semplici)

> Implementazione: Si realizza la soluzione aggiungendo gli aspetti astratti nella prima fase (ad esempio, si mostra come si possono risolvere i problemi più semplici)

questa implementazione e astrazione è utilizzata per creare macchine multilivello

nella tipica struttura a livelli, ogni livello superiore esegue il codice su una macchina virtuale inferiore eseguendo:  
- un interprete che viene eseguito eseguito su una macchina inferiore
- una traduzione nel linguaggio di una macchina inferiore

![](../img/livellimacchinevirtuali.png)

Tipico elaboratore a 6 livelli 
![](../img/elaboratore6livelli.png)

###  Livello 0

> porte logiche:  
> circuiti hanno tutti due input


### Livello 1

>Microarchitettura :  
> governa il flusso dei dati fra i vari componenti del livello logico digitale (può essere hardware o software)

### Livello 2

> Istruzioni macchina :  
> insieme di istruzioni eseguibili dalla microarchietettura

### Livello 3-4 

Livelli ibridi perchè non sono rigidamente separati

> sistema operativo:  
> fornisce la gestione di risorse ed esecuzione dei processi

> linguaggio assembly:  
> permette di programmare i livelli sottostanti

### Linguaggi 5

> Linguaggi di programmazione ad alto livello:  
> linguaggi che vengono compilati o interpretati, in linguaggio assembly

## Elaboratori

> Glie **Elaboratori** sono macchine multi-livello, e si utilizzano le astrazioni, e ogni volta vengono eseguiti o tradotti in nella astrazione sottostante 


## Storia degli Elaboratori


1. Pascalina: prima macchina del 1600 che faceva da calcolatrice
2. Analytical Engine: riusciva a fare somme con 50 cifre e una memoria di 1000 parole, ed è considerato il primo computer però non è stato mai costruito
3. colossus:si passa alle valvole al posto dei relè, ed è il primo computer funzionante
4. EINAC: misto tra relè e valvole, usato per scopi militari, si programmava cambiando i cavi e le schede perforate come input
5. IAS: progetto di un calcolatore, con la struttura che ancora viene utilizzata (formata da una memoria, una unità di controllo, unita aritmetico logica  e un input e output)
6. PDP-1: c'è il passaggio ai transistor, primo calcolatore ad avere un riscontro sul mercato, per la prima volta con un display
7. CDC 6600: è il primo calcolatore che poteva eseguire istruzioni in parallelo
8. IBM 360: multi programmazione (in memoria poteva avere più di un programma), diventa ancora più economico e si poteva comprare con diverse potenze
9. VLSI: è un cip con milioni di transistor (i precessori dei giorni nostri)
10. IBM 5150: primo personal computer che raggiungerà una veloce diffusione
11. Osborne1 il primo computer portatile
12. macintosh: primo con l'interfaccia grafica (senza lo schermo totalmente testuale)

il computing non è solo nel computer ma in molti altri oggetti

>**MIPS**: milioni di operazioni al secondo

>**MFLOPS**: miliardi di operazioni a virgola mobile
