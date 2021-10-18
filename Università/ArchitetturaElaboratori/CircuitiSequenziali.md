# Circuiti sequenziali

I **circuiti sequenziali** sono circuiti il cui risultato cambia in base agli input presi in passato

## Latch SR


TODO:aggiungere  descrizione  
TODO:aggiungere  l'immagine

## Latch SR temporizzato

TODO:aggiungere  descrizione  
TODO:aggiungere  l'immagine

## Latch D temporizzato

TODO:aggiungere  descrizione  
TODO:aggiungere  l'immagine


## Implementazione di DFF

TODO:aggiungere  descrizione  
TODO:aggiungere  l'immagine

tabella di verità

| in  | load | cl  | out[n]   |
| --- | ---- | --- | -------- |
| 0   | 0    | FS  | out[n-1] |
| 1   | 0    | FS  | out[n-1] |
| 0   | 1    | FS  | 0        |
| 1   | 1    | FS  | 1        |


> molte volte per realizzare un circuito sequenziale viene utilizzato un circuito combinatorio, che va in un flip-flop per poi tornare nell'input del circuito combinatorio


## Program counter 


```
if reset(t-1) then out(t)=0
else if load(t-1) then out(t)=in(t-1)
else if inc(t-1) then out(t)=out(t-1)+1
else out(t)=out(t-1)
```


## Memoria 

Una memoria con n locazioni da w-bit, può essere realizzata con n “w-bit register” controllati da uno specifico circuito, che indica da quale di questi registri deve essere letto.

(utilizzeremo un demultiplexer per il load e un multiplexer per l'out)



TODO: aggiungere immagine