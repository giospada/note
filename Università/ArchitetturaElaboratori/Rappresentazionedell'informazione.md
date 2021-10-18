
# 6. Rappresentazione dell'informazione

I calcolatori elaborano molti tipi di informazione come testi, immagini ,suoni ,numeri etc.. Nonostatne ciò le memorie dati possono contenere solo valori binari.

## 6.1. Numeri

Partiamo dai numeri naturali positivi che vengono rappresentati semplicemente in base 2.  


### 6.1.1. Modulo e segno

Moduloe segno si una l'ultimo bit come segno

> es
> usando 8 bit: 00000110=6, 10000110=-6

### 6.1.2. Complemento a 1

Complemento a 1: il bit più a sx indica il segno, ma se il numero è negativo il modulo viene complementato

>Es
> usando 8 bit: 00000110=6, 11111001=-6

### 6.1.3. Complemnto a 2

Complemento a 2: come per il complemento a 1, ma se il numero è negativo dopo il complemento si aggiunge 1

<details>
    <summary>
Esempio
    </summary>
usando 8 bit: 00000110=6, 11111010=-6
</details>

con questo metodo è più facile fare le addizzioni perchè riusciamo a farle con lo stesso metodo

con il complemento a 2 possiamo avere un range da $[2^{k-1}...2^{k-1}-1]$ dove k è il numero di bit

### 6.1.4. Codifica in eccesso

> La decodifica si ottiene applicando la decodifica 
standard e poi sottraendo $2^{k-1}$  al numero ottenuto

<details>
    <summary>
    esempio
    </summary>

00...00 rappresenta $-2^{k-1}$  
10...00 rappresenta $0$   
11...11 rappresenta $2^{k-1}$  
</details>

### 6.1.5. Numeri con la virgola

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



