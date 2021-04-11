
# Software Security

ELF: executable and linkable format

GCC: compilatore per il c

inizialmente trasoforma il l'eseguibile linkando le librerie e eseguendo
le macro `gcc -E prova.c`

poi il codice preprocessato è tradotto in assembly `gcc -S prova.c` 

per farlo diventare object code `gcc -C prova.c` (non è un eseguibile)


Linkaggio:
- statico: produco un unico eseguibile con tutte le dipendenze
- dinamico: che durante la esecuzione si linkano a librerie nel sistema


sezioni:
- .text:instruzioni del programma
- .bss:variabili senza inizializzazione
- .data: contengono i dati inizializati
- .rodata sono dati readonly
- .symtab: simboli che il programma utilizza
- .dynamic: informazione per il linking

## readelf

un comando per vedere gli eseguibili


