
# Insiemi numerici, e le loro proprietà


**numeri naturiali** : $N =\{1,2,3,4...\}$   

**numeri interi** : i numeri interi hanno la proprietà di avere l'opposto,  $Z =\{..-2,-1,0,1,2,...\}$ 

**numeri razionali** : ogni unmero ha l'opposto e l'inverso, $Q =\{\frac{p}{q} | p \in N, q \in Z, p \neq 0 \}$  
$Q = \{ \frac{n}{m} | n \in N, m \in Z \backslash \{0\}, MCD(n,|m|)=1\}$

**numeri reali** :  $R$

## Notazioni

|                           symbolo                           |                            spiegazione                            |
| ----------------------------------------------------------- | ----------------------------------------------------------------- |
| $\in$                                                       | Indica che un elemento appartiene ad un insieme                   |
| $\notin$                                                    | non appartiene                                                    |
| $\forall$                                                   | per tutti gli elementi di un insieme                              |
| $:$ oppure \|                                               | tale che                                                          |
| $\exists$                                                   | Esiste almeno un elemento                                         |
| $\nexists$                                                  | Non esiste neanche un elemento                                    |
| $\exists!$                                                  | Esiste un solo elemento                                           |
| $\subseteq$                                                 | $A \subseteq B$ indica che A è un sottoinsieme o uguale a B       |
| $\nsubseteq$                                                | $A \nsubseteq B$ c'è almeno un elemento in A che non è in B       |
| $\cup$                                                      | unione tra due iniemi                                             |
| $\cap$                                                      | crea un insieme con gli elementi comuni dei due insiemi           |
| $\emptyset$                                                 | insieme vuoto (è un subset di tutti gli insiemi)                  |
| $\backslash$                                                | differenza tra insiemi (non è commutativa}                        |
| $\upsilon$                                                  | inisme universo è un insieme definito per fare il complementare   |
| $C(A)$                                                      | diffrerenza tra un insieme universo e l'insieme A (complementare) |
| $\wedge$                                                    | E logioco (and)                                                   |
| $\vee$                                                      | O logioco (or)                                                    |
| $\implies$                                                  | è il simbolo di implicazione logica                               |
| $\bar{p}$                                                   | è la negazione della preposizione p                               |
| $\displaystyle \sum_{i=0}^n a_i= a_0 + a_1 + a_2+ ... +a_n$ | sommatoria                                                        |



## Insiemistica 

> un insieme è definito dai suoi elementi, e non dal loro ordine 

### Operazioni

TODO: da finire di aggiungere le operazioni e scrivere la loro definizione

**Unione Insiemi**: crea un insieme contenente tutti gli elementi di a A e B
A,B sono insiemi  
$A \cap B = \{x | x \in A \vee x \in B \}$  

**Unione Insiemi**: crea un insieme contenente tutti gli elementi comuni a A e B
A,B sono insiemi  
$A \cap B = \{x | x \in A \wedge x \in B \}$  


**Sottrazione tra Insiemi**: Dati due insiemi A e B crea un insieme che contiene tutti gli elementi di A che non appartengono in B

$A \backslash B =\{x| x \in A \wedge x \notin B \}$

**Moltiplicazione Insiemi**(prodotto cartesiano): associa ogni elemento dell'insieme A tutti gli elementi dell'insieme B creando delle coppie ordinate
A,B sono insiemi  
$A$ x $B$ = $\{ (a,b) | a \in A \vee b \in B\}$  
$A$ x $B \neq B$ x $A$
