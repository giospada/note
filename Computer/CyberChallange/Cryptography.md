
# Cryptography

è il sistema utilizzato per data integrity authentication cofidentiality e non reputation

è una scenza matematica che studia la trasofmazione dei dati che si divide in tre classi:

- simmetrica : chiave segreta
- asimmetrica:a chiva privata e pubblica (è più recente e viene proposta a metà degli anni 70)
- hash: strumenti di tipo crittografico che sono delle funzioni per generare una stringa di bit univoca



## 1

**Chive simmetrica**
chimata clasica o a chiave singola
poichè si possono fare le due funzioni 
di criptagio e decriptaggio con la stessa chiave
ogni algoritmo prende un testo e una chiave 
e nessuno riesce a decriptarlo senza l'algorimo e la chiave

tipi di cipher:
- blocchi: testo in chiaro a blocchi tipo 16 byte
- stream: cifra con i byte 


criptaggio

plain text (m)

ciphertext (x)

key(k)

chipher algoritmo che lo trasforma 

criptaggio
$c = E(k,m)= $

decriptaggio
$m=D(k,c) = D(k,E(k,m))$

tipi :
DES,3DES,RC4,IDEA,AES


per la chive simmetrica 
le parti devono condividere la stessa chiave
che bisogna per forza condividere attraverso un canale sicuro 

tipi di attacco :
- l'attaccante piò solo analizzare il testo cifrato Ciphertext-only
- ha il testo cifrato e quello non Known-plaintenxt
- può scegliere il testo in chiaro chosen-plaintext
- può scegliere il testo cifrato chosen-ciphertext


tipi di attcco:
- cripto analisi: cerca delle vulnerabilità nel algoritmo che conosce
- forza bruta: provare tutte le possibilità (dictioray sono quelli che sono più probabili)( se si sa m/c)
- side-channel: usa le informazioni correlate all'operazione di criptaggio e decriptaggio(es:timing attack,tepest,power monitoring attack)

#### Sobstitution Ciphers 

algoritmi che criptano andando a sostituire con dei caratteri con altri 

sono usati o in cifrari molto vecchi o in cifrari come subrutine di cifrari moderni
per complicarne la complessità

es Caesar cipher

dove ogni lettera viene sostitita con quella una successiva di un numero fissato

$C= E(P)= (P+k) mod 26, con k=3$<br>
$P= E(C)= (P-k) mod 26, con k=3$

monoalphabetic substitution ciphers

la chiave è la stringa di sostituzione
dove ogni lettera è uguale ad un altra 
quindi le chiavi possibili sono 26! 

attacchi:
- letter frequencies
- two letter frequencis
- most common words

Polyalphabetic sobstitution: vigenere

oltre a ad utilizzre la lettera utilizza la posizione applicando uno shift costante 

**one time pad**

dato un testo in chiaro lo cifra con una chiave altrettanto lunga e per ogni simbolo lo shift
fa l'opzione di zor



techniche che sostituiscono 


trasposion ciphers 

riarrangia le lettere senza alterare le lettere usate

la chiave riappresenta la permutazione


Product ciphers

questi algoritmi usano sostituzione e traspsizioni più volte aumentando la complessità ogni volta 



a blocchi o stream 

stream : prende un messaggio di lunghezza variabile 

di solito si parte da una chiave che genera una sequenza di caratteri infinita e fa 
semplicemente l'xor dei bit in input

blocchi:cripta ogni blocco

feistel: diversi round dove vengono create chiavi di valore diverso


AES utilizza SP-network (sobstitution and permutation)



CBC usa fa xor con un vettore inizzializzato e poi cripta fa l'xor con il blocco 
precedente  

- OFB
- CTR


# Crittografia assimmetrica


doppia chiave

usano funzione matematiche facendo diventare i bit in numeri 
e ritrasformali


funzione trapdor f(x)=y computare f-1(y)=x è molto difficile

es di f(x) il prodotto tra due numeri primi mentre f-1(x) è NP

## RSA


quello più flessibile

è bastao sull'aritmetica modulo n se n è molto grande

operazioni su interi

1024 bit per una chiave circa 10^308

- si prendono due numeri primi molto grandi( tipo 512 bit) 
 (denominati p e q)
- il loro prodotto è n p*q=n
- si computa fi(n)=(p-1)*(p-1)
- gcd(e,fi(n))=1
- si trova un numero d che è il motilpicativo inverso di e mod fi(n)
- chiave pubblica KU=K+=<e,n>
- chiave privata KR= K-=<d,n> 

(e è un modulo fissato) e*d mod fi(n) = 1 / e*d=1 (mod fi(n))

criptare 
c= m^e mod n


decriptare 
m=c^d mod n


se m è facile da scoprire può fare dei tentativi di criptaggio

