
# Rappresentazione dell'informazione

I calcolatori elaborano molti tipi di informazione come testi, immagini ,suoni ,numeri etc.. Nonostante ciò le memorie dati possono contenere solo valori binari.

## Numeri

Partiamo dai numeri naturali positivi che vengono rappresentati semplicemente in base 2.  


<details>
<summary>
esercizio
</summary>

Si consideri il numero decimale 35 (senza segno).
Lo si converta in binario, poi dal binario in esadecimale, e dall'esadecimale di nuovo in decimale.

35=100011b=23hex
</details>

### Modulo e segno

Modulo e segno si una l'ultimo bit come segno

> es
> usando 8 bit: 00000110=6, 10000110=-6

### Complemento a 1

Complemento a 1: il bit più a sx indica il segno, ma se il numero è negativo il modulo viene complementato

>Es
> usando 8 bit: 00000110=6, 11111001=-6

### Complemnto a 2

Complemento a 2: come per il complemento a 1, ma se il numero è negativo dopo il complemento si aggiunge 1

> Esempio  
> usando 8 bit: 00000110=6, 11111010=-6

con questo metodo è più facile fare le addizioni perchè riusciamo a farle con lo stesso metodo

con il complemento a 2 possiamo avere un range da $[2^{k-1}...2^{k-1}-1]$ dove k è il numero di bit

### Codifica in eccesso

La decodifica si ottiene applicando la decodifica 
standard e poi sottraendo $2^{k-1}$  al numero ottenuto

> Es   
> 00...00 rappresenta $-2^{k-1}$  
> 10...00 rappresenta $0$   
> 11...11 rappresenta $2^{k-1}-1$  

<details>
<summary>
Esercizio
</summary>

Si consideri il numero decimale -13.  
Lo si converta in binario (su 8 bit) con le codifiche:
  
- modulo e segno
- complemento a 1
- complemento a 2
- eccesso 128


- modulo e segno : 10001101
- complemento a 1: 11110010
- complemento a 2: 11110011
- ad eccesso 128 : 01110011
</details>

### Numeri con la virgola

la rappresentazione dei numeri con la virgola si usano due numeri:
- f che è la mantissa
- e che è l'esponente

$n=f \times 10^{e}$

<details>
  <summary>
  esempio codifica
  </summary>

se la mantissa è tra 0,001 e 0,999
e l'esponente è tra 0 e 99

riesco a rappresentare i numeri

![](../img/overflowunder.png)

</details>

**notazione concreta**:
- utilizziamo la base 2
- come mantissa utilizziamo un numero minore di 1
- inoltre normalizziamo la mantissa (la cifra più significativa (dopo la virgola) non può essere uguale a zero)

<details>
  <summary>
esempio concreto
  </summary>

vogliamo rappresentare il numero 432:  
la mantissa sarà 432=110110000b questo numero va normalizzato quindi dobbiamo shiftarlo, quindi gli diamo un esponente di: $2^9$

</details>

**standard binary32**:
- 1 bit di segno
- 8 bit di esponente
- 23 bit di mantissa

<details>
  <summary>
Si converta il numero 0.3 in notazione floating point in base 2 normalizzata (usando il complemento a 2 su 8 bit sia per la mantissa che per l'esponente).
  </summary>

  TODO: da finire


la mantissa si legge moltiplicando il primo partendo da sinistra $2^-1$ fino a $2^-n$ nell'ultimo dove n sono il numero di bit, e per calcolare il numero in decimale va tutto moltiplicato per $2^{\text{esponente}}$

segno : 0 
mantissa: 10011001b
esponente: 1111111b

</details>


## Stringhe

### ASCII

> American standard code for information interchange

Questa è la **prima codifica dei caratteri, usa i primi 7 bit** per i principali simboli alfabetici anglosassoni e per alcuni caratteri speciali.

### Unicode

**Estende** la codifica **ASCII** aggiungendoci **altri alfabeti**, aumenta la lunghezza a **16 bit** e rimane compatibile con la codifica ASCII (mettendo i primi 9 bit a 0).


### UTF-8

Essendo che la codifica **unicode è all'esaurimento** dei possibili codici, e **usa 16 bit** anche per i caratteri asci; Si è sviluppata la **UTF** che può dinamicamente occupare **da 1 a 4 byte** a seconda dell'informazione; **rimane compatibile con ASCII**, infatti se il primo bit è a zero significa che il carattere è un carattere ascii e che occuperà i prossimi 7 bit.

## Codici corretti

Memorie e trasmissioni di dati sono soggette ad errori, così si creano dei codici di controllo:  
- m bit: della parola
- r bit: di controllo, scelti in un meccanismo
- n bit: m+r "parola codice"


> **la distanza di hamming** è la differenza di bit tra due stringhe di bit.
(es: distanza tra 101110 e 110101 è 4)

**Regola generale:**  
- Per rilevare d  bit errati è necessario un codice con distanza di Hamming maggiore o uguale a d+1
- Per correggere d  bit errati è necessario un codice con distanza di Hamming maggiore o uguale a 2d+1

### Bit di parità

Il codice è composto da un solo bit di controllo (r=1), se la parola ha i bit "1" di numero pari allora il bit di parità è a 1.(distanza Hamming 2)

Il codice rileva se c'è un singolo bit errato.

### Codice d'esempio

Inventiamo un nuovo codice di 4 parole:0000000000-0000011111-0000011111-1111111111  
Questo questo codice ha una distanza di hamming di 5 quindi è possibile correggere fino a due errori.

TODO: finire