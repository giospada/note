# HashMap

**Tabella Hash** è un implementazione della struttura dati Dizionario con: `insert`,`serach` e `delete` in $O(1)$


## Costruzione

**Indichiamo**: 
- $U$ insieme universo (tutte le chiavi possibili)
- $K$ chiavi effettivamente utilizzate


> NOTA
> se la cardinalità di K è molto vicina a quella di U convienei  utilizzare un indicizzamento diretto
>   
> se la cardinalità di K è molto più piccola possiamo utilizzare un **HashTable**


Per creare la **tabella hash abbiamo bisogno** di:
- **funzione di Hash**  
- metodo per **gestire le collisioni**
- un **vettore di dimensione** $m=\Theta(|K|)$

## Funzioni Hash (esempi)

metodi per creare l'hash:
- **modulo per un numero primo**
- **moltiplicazione** per esempio utilizzando la formula $\lfloor m* (kC-\lfloor kC \rfloor)\rfloor$ (C è una costante tra 1 e 0 ) il valore C è un valore buono è $(\sqrt{5}-1)/2$  perchè è uniforme
- **codifica algebrica** $(k_nx^n + k_{n−1}x ^{n−1} +\dots + k_1x + k_0) \mod m$


## Problema delle collisioni

### Concatenamento

**concatenamento**: le chiavi con lo stesso hash vengono memorizzate attraverso una lista concatenata 

### Inidirizzamento aperto

**indirizzamento aperto** tutte le chiavi sono sullo stesso array, per scegliere la posizione degli hash giù utilizzati si utilizza la funzione hash modifica per prendere un indice 

Metodi di ispezionamento:
- **ispezione linerae** semplicemente si prende una  funziona hash ci sia aggiunge l'indice  e  si fa il modulo con il numero di celle libere ($h(k,i)=(h'(k)+i )\mod m$ dove i è l'indice h' è la funzione di hash e m è il numero di celle) 
- **ispezione quadratica** ($h(k,i)=(h'(k)+ic_2+i^2c_1) \mod m$ e dove le c sono due  costanti diverse tra loro, e m è la dimensione della tabella)
- **doppio hash** ($h(k, i) = (h_1(k) + ih_2(k)) \mod m$ dove m è la dimensioni della tabella e h_1 e h_2 sono due funzioni hash, h_2 non deve dare come valore 0)
 
