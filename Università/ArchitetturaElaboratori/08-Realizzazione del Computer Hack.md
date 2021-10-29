# Realizzazione del Computer Hack

##  Tastiera

Tastiera è una memoria ROM in solo lettura


##  Schermo

Lo Schermo è come una memoria ram, tutto quello che vieine scritto su questa memoria appare nella schermo del simulatore.

Lo schermo è diviso in colonne   e righe


## Codifica A-instruction

![](vx_images/2106204199297.png)


## Codifica C-Instruction

![](vx_images/5357587756820.png)


## Livello Istruction Set Architeture

> ISA è l'interfaccia tra l'hardware e il software, i compilatori traucono i programmi in instruzioni livello ISA

In generale le istruzioni sono divise in:
- **codice operativo**: parte che indica il tipo di istruzione da eseguire
- **indirizzi**: indicano gli operatori da utilizzare

![](vx_images/2558021179300.png)

Gli indirizzamento:
- Indirizzamento immediato: L’istruzione include già l’operando da usare (vedi A-instruction del linguaggio Hack)
- Indirizzamento diretto: L’istruzione contiene l’indirizzo completo in memoria della cella in cui reperire l’operando
- Indirizzamento a registro: L’operando viene prelevato da un registro
- Indirizzamento a registro indiretto: L’operando viene prelevato dalla memoria, all’indirizzo puntato da un registro (vedi l’accesso in memoria del linguaggio Hack, con “indirizzamento a registro indiretto” tramite registro A)

Indirizzamoento a stack: i processori hanno delle istruzioni per gestire lo stack, come push, pop + dei registri dedicati BSP ..

Tipiche istruzioni:
- operandi di trasfermiento dati: È trasferiscono dati da memoria a registri e viceversa e da registri a registri
- operazioni aritmetico-logiche: Operazioni su interi e floating-point
- operazioni unairie: (prendono un solo operatore) per esempio le instruzioni shift o inc
- salti: condizionati e non
- alcuni compilatori hanno