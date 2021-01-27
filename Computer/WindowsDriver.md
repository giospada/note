---
tags: [Computer]
title: WindowsDriver
created: '2020-01-07T18:29:42.820Z'
modified: '2020-05-30T17:01:43.260Z'
---

# WindowsDriver
## [kernel vs user mode reference ](https://docs.microsoft.com/en-us/windows-hardware/drivers/gettingstarted/user-mode-and-kernel-mode)
kernel e user mode sono i duei differenti modi in cui il processore esegue 
i driver possono essere eseguiti in entrambi i modi
#### user-mode application
user-mode application  hanno una memoria virtuale e private hendle table ogni applicazionione quidi ha il proprio spazio di esecuzione distinto dalle altre infatti se crasha succede solo a quella appilcazione
inoltre questo tipo di processi non possono accedere agli virtual addresses che è riservato al os 
#### kernel
tutto il codeice che viene eseguito in kernel mode usa un solo virtual address space : che significa  che ol kernel-mode driver non sono isolati tra loro e neanche con il kernel
se un kernel-mode driver crasha crasha l'os

## [Virtual address spaces](https://docs.microsoft.com/en-us/windows-hardware/drivers/gettingstarted/virtual-address-spaces)

#### Virtual address spaces

quando il processore scrive o legge verso un area di memoria usa i virtual address.
nella read/write operaion il processosore traduce il virtual addrdress in un addresss fisico.
accedendo da un indirizzo virtuale ci sono vantaggi
-  un programma può utilizzare un range continuo di virutal adress che nella memoria reale non è continuo
- Un programma può utilizzare un intervallo di indirizzi virtuali per accedere a un buffer di memoria più grande della memoria fisica disponibile. Man mano che la quantità di memoria fisica si riduce, il gestore della memoria salva pagine di memoria fisica (in genere 4 kilobyte) in un file su disco. Le pagine di dati o codice vengono spostate tra la memoria fisica e il disco secondo necessità

virtual address space è il range di virtuali indirizzi disponibili. ogni processo user-mode ha il proprio virtual address space che di solito è di 2 gigabyte da 0x00000000 a 0x7FFFFFFF (processi 32). per i prcessi a 64 bit la memoria virtuale è da  0x000'00000000  a 0x7FF'FFFFFFFF per un totale di 8-terabyte range.
#### User space and system space

32 bit ha un totale di vitual address space di 2^32(4 gigabytes(i computer a 32 bit non possono avere più di 4 GB di ram)). di solito sono divisi a metà tra user e system space.

![Icon](@attachment/virtualaddressspace02.png)

ivece quelli a 64 bit hanno 2^64 cioè (16 exabytes) ma solo una piccola parte viene usata  8-terabyte range da  0x000'00000000 a 0x7FF'FFFFFFFF per user space,e 248-terabyte range da 0xFFFF0800'00000000 a 0xFFFFFFFF'FFFFFFFF per system space.

![Icon](@attachment/virtualaddressspace03.png)

Il codice in esecuzione in modalità kernel ha accesso sia allo spazio utente che allo spazio di sistema(user mode process sono al loro). Cioè, il codice in esecuzione in modalità kernel ha accesso allo spazio di sistema e allo spazio di indirizzi virtuale dell'attuale processo in modalità utente.



