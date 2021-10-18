# Microarchitettura

TODO:add hack processore schema

![](../img/microarchitettura.png)

- instruction:prende l'istruzione
- reset:fa il reset del program counter e fa ricomiciare il programma dall'inizio
- outM:è un bus che va in memoria

- Un **registro D** che contiene uno dei due operandi della ALU, e che può memorizzare
un precedente output
- Un **registro A** che può contenere un dato che fa parte delle istruzioni o un precedente output
- Il **secondo input della ALU** può essere o il contenuto del registro A oppure un dato proveniente dalla memoria
- E’ presente anche il **Program Counter** che, per quanto riguarda i salti, può essere impostato tramite il registro A
- Il registro A può essere anche usato come **puntatore alla memoria** (per operazioni di lettura/scrittura)
- Il flusso dei dati fra i vari componenti viene controllato tramite Mux 
- I **Mux ed i bit di controllo dei registri**, vengono gestiti da una microarchitettura composta da semplici circuiti combinatori
- Infatti, **l’intero ciclo Fetch-Decode-Execute del processore Hack viene eseguito in un solo ciclo** di clock, ed i segnali di controllo sono funzione dell’istruzione corrente
  - In altre parole, una istruzione in ingresso al tempo t, viene completamente eseguita entro il tempo t+1
  - Al tempo t+1 viene considerata l’istruzione successiva 


Il decode setta i c bit che vengono utilizzati come control bit per tutti gli altri componenti

TODO: finisci di spiegare il tutto 


## SRAM e DRAM

Le **SRAM** (Static RAM) sono realizzate tramite flip-flop come le memorie viste in precedenza
- Veloci (ordine del nanosecondo)
- Usate principalmente per le cache

Le **DRAM** (Dynamic RAM) o SDRAM (Synchronous DRAM), usate per le memorie centrali, hanno un solo transistor ed un condensatore che mantiene (tramite carica elettrica) un singolo bit

-Visto che il condensatore perde la propria carica, deve essere ricaricato per evitare di perdere la propria informazione
- Si rendono necessarie periodiche fasi di “refresh” (ad intervalli dell’ordine del millisecondo)
  - A causa del refresh sono più lente (ordine della decina di nanosecondi)
  - Richiedendo un solo transistor costano meno e possono essere maggiormente miniaturizzate