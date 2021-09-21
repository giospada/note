# Architettura degli Elaboratori

> 20/09/2021


## Porte logiche 

hanno tutti due input

un circuito si scrive anche con una tabella di verità

>`tabella di verità` mappa tutti gli input con i risultato l'output (ha $2^n$ righe)

(si costruirà tutto partendo dalla porta NAND, e utilizzando solo questo circuito)

### NAND

> si usa la NAND perché si possono realizzare tutte le funzioni logiche booleane


`NAND` = and binario

# Circuiti combinatori


sono circuiti che con lo stesso set di input input  producono lo stesso output

## Circuiti Sequenziali

Circuiti che cambiano l'output in base agli input ricevuti in passato

## Microarchitetture

governa il flusso dei dati fra i vari componenti del livello logico digitale

## Istruzioni macchina

insieme di istruzioni eseguibili dalla microarchietettura



## Elaboratori

sono macchine multi-livello, e si utilizzano le astrazioni, e ogni volta vengono eseguiti o tradotti in nella astrazione sottostante 


## Libri

- Architettura dei calcolatori. Un approccio strutturale

[DA SCARICARE](http://www.nand2tetris.org)


## Esame

- esame scritto (27 punti) dove si avranno punti bonus per i progetti (max. 6) e per li interventi


## Lezione 1 (21/09/2021)

### Storia degli Elaboratori

> non sono per l'esame

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


### Organizzazione degli Elaboratori

![](img/VonNeumann.png)
> "bus oriented": un bus è un insieme di connessioni elettriche per collegare i vari componenti

IL bus a differenza dello schema di van Neumann, non ha una connessione punto a punto ma tutti i componenti sono collegati al bus 

Una altra novità è che con von Neumann la memoria non solo per i dati ma anche per i programmi 

La cpu e la memoria utilizzano i **bus dati** e il **bus indirizzi** per scambiarsi le informazioni

![](img/bus.png)

### CPU

![](img/cpuschema.png)

> la cpu è il cervello della macchina che esegue i calcoli

**la cpu è composta da**:
- unita di controllo:legge e interpreta le istruzioni 
- alu: esegue le operazioni
- registri: che sono delle celle di memoria per i dati necessari al funzionamento

la memoria centrale è più lenta del processore, e come primo accorgimento si utilizzano i registri per tenere i dati più utilizzati

**Registri Speciali**(non "general propose" di uso generale):
- Program Counter:indica la prossima istruzione
- Instruction Register: contiene l'istruzione che stiamo eseguendo
- Memory registers:si usano per interagire con la memoria
    - Memory address Register: su questo si mette l'indirizzo da leggere o scrivere  
    - Memory data Register: qui si scrive li dato da scrivere o si legge il dato appena letto
- Program Status Word: indica informazioni sull'andamento dell'ultima istruzione eseguita (c'è stata un'overflow, l'ultima operazione è risultata zero)

**Esempio pratico dell'esecuzione di un istruzione**  
1. il contenuto di Program counter viene messo su Memoriy addre Register e viene letta l'istruzione
2. la memoria copia il contenuto della cella all'indirizzo del Memory address register su il Memory Data Register
3. il contenuto di Memory Data Register viene copiato su Instruction Register
4. l'istruzione passa all'ALU
5. se ci sono operatori da prelevare in memoria si collegano a i registri (utilizzando sempre il Memory Address Register e il Memory Data Register)
6. termina l'esecuzione e il risultato va sul registro di destinazione (aggiorna il Program Status Word), e se bisogna scrivere la memoria scrive in memoria il valore calcolato si sposta sulla memoria utilizzando sempre il MDR e il MAR
7. si torna al punto 1 dopo avere aggiornato il valore di Program Counter

> il program counter viene incrementato in modo diverso dal tipo di architettura, alcuni sistemi hanno una dimensione fissa dell'istruzione e a quel punto incrementa di una costante, in altri casi quanto si hanno diversa lunghezza nelle istruzioni un circuito nel processore sa di quanto incrementare in base all'istruzione eseguita

il ciclo di esecuzione può essere schematizzato anche come **FDE**:
1. **Fetch**  caricamento della memoria di un'istruzione (punti 1-2 dell'esempio)
2. **Decode** identificazione del tipo di operazione da eseguire (punto 3) 
3. **Execute** effettuazione delle operazioni corrispondenti all'istruzione (punti 4-5-6)

#### Unita di controllo

> l'unita di controllo gestisce la memoria e l'alu, e interpreta le istruzioni

i tipi di set di istruzioni possono essere:
- CISC: Complex Instruction Set Computer, e quindi utilizzare microprogrammazione e un processore più complesso
- RISC: Reduced Instruction Set Computer, istruzioni più semplici possono essere eseguite più velocemente e potendo evitare la microprogrammazione

 

nel calcolatore c'è un segnale che si chiama clock, che è un segnale regolare che da il tempo ad eseguire le istruzioni (un operazione può utilizzare anche più cicli di clock) 


