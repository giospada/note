

# Task Warrior

un terminal application estesa con verie librerie che 
serve pre tenere le todo list da terminale 

**SINTASSI**

> task [ filtri ] [ comandi ] [ modificatori ] [ varie]

**filtri** servono per selezionare un insieme di task (senza sono tutte)
si possono mettere alla destra del comando solo se il comando non 
accetta modificatori o varie


### Linkig

### Concetti

**Project** un progetto può avere più task ma 
una task può avere un solo progetto


### Incominciamo

> task

mostra la lista delle task in corso

> task add  Descrzione 

aggiunge una task con la descrizione


> task number done

elimina la task segnata con il numero

### Tag

> task add  Descrzione  +tag

aggiunge una task con la descrizione e con quel tag

> task +LATEST modify -prova -prova2

modifica l'ulima task editata o creata togliendo il il tag 
prova e mettendo il tag prova 2

> task +tag

fa vedere tutte le task con il tag

> task -tag

fa vedere tutte le task senza il tag

### Special Tag

+LAST
+YEAR



