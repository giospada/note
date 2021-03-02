
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









