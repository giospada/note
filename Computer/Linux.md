---
tags: [Computer]
title: Linux
created: '2020-04-07T07:48:27.233Z'
modified: '2020-05-30T17:01:50.575Z'
---

# Linux
> prova a tenerlo aggiornato con tutti i comandi che usi e aggungendoli con anche le flag
## Cos'è
è un sistema multiutente creato da linus travold 
è un sistema UNIX-like
## Command Line
### la shell
la shell è un programma che prende dalla tastiera degli input e li manda al sistema operativo
### Comandi principali
- `pw` : scrive la direcory corrente
- `cd` : cambia directory
- `ls` : mostra i file in una directory flasg(a mostra i file nascosti, l mostra i dettagli cioè i permessi il nome del proprietario il gruppo etc..)
- ` touch` : aggiorna l'ultima data di modifica di un file se non c'è il file lo crea  
- `file` : scrive che tipo di file è
- `cat` : ridirige lo stdin verso std out se si aggunge uno o più file come argomento scrive in stdout il contenuto dei file
- `less` : è per vedere il contenuto di un file grande pochè si può scorrere cercare 
- `history` : scrive in stdout i comandi eseguiti in precedenza
- `cp` : copia 1 o più file in una directory flag(r recursive copia tutti i file nella directory)
- `mv` : sposta dei file 
- `mkdir` : crea delle directory flags(p se si vuole creare una serie di subdirectory)
- `rm` : elimina uno o più files flags(r recursive(tutte le sub dir),)
- `find` : 
- `locate` : localizza un file a differenza di find lo tiene in un db aggiornato si può aggiornare il db con updatedb
- `man` : mostra il manuale di un comando
- `whatis` : descrive cosa fa un comando
- `alias` : fa vedere gli alias flag( nome="valore" crea un alias che si richiama con nome ed esegue il comando valore) unalias nome toglie l'alias
- `env` : elenca tutte le varibili 
## Working with file
### redirection
- `command > file` : ridirige l'stdout del command nel file (riscrivendolo)
- `command >> file` : ridirige l'stdout del command alla fine del file file(aggungendo)
- `command < file` : prende lo stdin del command dal file
- `command 2> file` : scrive solo stderr nel file
- `command &> file` / `command > file 2>&1` : ridirige sia  lo stdout che lo stderr in f
- `command1 | command2 ` : ridirige lo stdout dell command1 nel stdin del command2
- `tee` :ridurige lo stdin in stdout e un file come argomento utile con le pipe
### file manipulation
- `cut` : modificare l'input flags(c con un range scrive le lettere del range num1-num2, f prende il range di colonne delimitate dal delimitatore,d setta il delimitatore di default TAB )
- `paste` : combina le righe con un delimitatore(default TAB) flags(d delimitaotre )
- `head` : mostra le prime 10 righe di un file fags(n per modificare il numero di linee)
- `tail` : mostra le ultime 10 line di un file flags(n per modificare il numero di linee, f per vedere aggunte in live)
- `split` : divide un file in più file 





