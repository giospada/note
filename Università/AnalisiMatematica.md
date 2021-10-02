---
title: Analisi Matematica
date: Settembre 2021
author: Giovanni Spadaccini
---
- [1. Introduzione](#1-introduzione)
  - [1.1. Requisiti](#11-requisiti)
  - [1.2. Modulo 1](#12-modulo-1)
  - [1.3. Modulo 2](#13-modulo-2)
  - [1.4. Esame](#14-esame)
    - [1.4.1. Sessioni](#141-sessioni)
- [2. Insiemi numerici, e le loro proprietà](#2-insiemi-numerici-e-le-loro-proprietà)
  - [2.1. Notazioni](#21-notazioni)
- [3. Insiemistica](#3-insiemistica)
- [4. Logica](#4-logica)
- [5. Funzioni](#5-funzioni)
  - [5.1. Cardinalità](#51-cardinalità)
  - [5.2. Numberailità](#52-numberailità)
- [6. Calcolo Combinatorio](#6-calcolo-combinatorio)
  - [6.1. Coefficente Binomiale](#61-coefficente-binomiale)
  - [Il binomio di Newton](#il-binomio-di-newton)
- [Teorema di pitagora](#teorema-di-pitagora)
- [L'insieme dei numeri razionali](#linsieme-dei-numeri-razionali)

# 1. Introduzione

Insegnante: Marco Maghetti

`marco.maghetti@unibi.it`

[Materiale](https://virtuale.unibo.it/course/view.php?id=28828)


## 1.1. Requisiti

- algebra elementare
- equazioni algebriche
- disequazioni di primo e secondo grado
- disequazioni frazionarie
- equazioni e disequazioni goniometriche elementari
- equazioni e disequazioni logaritmiche e esponenziali
- elementi di geometria analitica


## 1.2. Modulo 1

- Insiemi numerici, e le loro proprietà
- Funzioni elementari (esponenziali,logaritmi,trigonometria)
- successioni numeriche
- Limiti
- Funzioni per la cardinalità
- funzioni derivabili
- grafico di una funzione
- formula ti Taylor per le funzioni regolare

## 1.3. Modulo 2

## 1.4. Esame

1. prova scritta (che serve per entrare all'orale) esercizi + alcune domande di teoria
2. prova orale (deve essere passata nella stessa sessione ma anche in appelli differenti)

### 1.4.1. Sessioni

ci sono quattro sessioni ed ogni sessione ha un gruppo d'appelli (esistono sessioni estive, autunnali e invernali).

il primo analisi ci sarà in giugno 2022.


# 2. Insiemi numerici, e le loro proprietà


**numeri naturiali** : $N =\{1,2,3,4...\}$   

**numeri interi** : i numeri interi hanno la proprietà di avere l'opposto,  $Z =\{..-2,-1,0,1,2,...\}$ 

**numeri razionali** : ogni unmero ha l'opposto e l'inverso, $Q =\{\frac{p}{q} | p \in N, q \in Z, p \neq 0 \}$  

**numeri reali** :  $R$

## 2.1. Notazioni

|symbolo       | spiegazione                                                   |
|--------      |-------------                                                  |
|$\in$         |Indica che un elemento appartiene ad un insieme                |
|$\notin$      |non appartiene                                                 |
|$\forall$     |per tutti gli elementi di un insieme                           |
|$:$ oppure \| |tale che                                                       |
|$\exists$     |Esiste almeno un elemento                                      |
|$\nexists$    |Non esiste neanche un elemento                                 |
|$\exists!$    |Esiste un solo elemento                                        |
|$\subseteq$   |$A \subseteq B$ indica che A è un sottoinsieme o uguale a B    |
|$\nsubseteq$  |$A \nsubseteq B$ c'è almeno un elemento in A che non è in B    |
|$\cup$        |unione tra due iniemi                                          |
|$\cap$        |crea un insieme con gli elementi comuni dei due insiemi        |
|$\emptyset$   |insieme vuoto (è un subset di tutti gli insiemi)               |
|$\backslash$  |differenza tra insiemi (non è commutativa}                     |
|$\upsilon$    |inisme universo è un insieme definito per fare il complementare|
|$C(A)$        |diffrerenza tra un insieme universo e l'insieme A              |
|$\wedge$      |E logioco (and)                                                |
|$\vee$        |O logioco (or)                                                 |
|$\rightarrow$ |è il simbolo di implicazione logica                            |
|$\bar{p}$     |è la negazione della preposizione p                            |
|$\displaystyle \sum_{i=0}^n a_i= a_0 + a_1 + a_2+ ... +a_n$| sommatoria |


TODO:finire di aggiungere le notazioni viste

# 3. Insiemistica 

> un insieme è definito dai suoi elementi, e non dal loro ordine 

<details>
    <summary>
        operazioni
    </summary>

TODO: da finire di aggiungere le operazioni e scrivere la loro definizione

**Unione Insiemi**: crea un insieme contenente tutti gli elementi comuni a A e B
A,B sono insiemi  
$A \cap B = \{x | x \in A \wedge x \in B \}$  

**Moltiplicazione Insiemi**(prodotto cartesiano): associa ogni elemento dell'insieme A tutti gli elementi dell'insieme B creando delle coppie ordinate
A,B sono insiemi  
$A$ x $B$ = $\{ (a,b) | a \in A \vee b \in B\}$  
$A$ x $B \neq B$ x $A$

</details>

# 4. Logica

> p = proposizione (è un affermazione che può essere o vera o falsa)

$\bar{p}$ = "non p", è la negazione di p


attezione :
- la negazione di tutti è esiste almeno un elemento $\bar{\forall}$ = $\exists$  
- la negazioni di esiste almeno un elementeo è tutti  $\bar{\exists}$ = $\forall$

<details>
    <summary>
        esempi
    </summary>

es.
p = ogni elemento di A è un numero pari  
$\forall a \in A : \text{a è pari}$   
$\bar{p} = \exists a \in A : \text{a non è pari}$ 
</detailS>


$p \rightarrow q$ = "p implica q" (p si chiama ipotesi e q si chiama tesi)

<details>
    <summary>
        tabella di verità e equivalenza
    </summary>


</details>


$p \leftrightarrow q$ = "p implica q" 

significa che $(p \rightarrow q) \wedge( q \rightarrow q)$

"è sufficiente p affinché q"

<details>
    <summary>
        tabella di verità
    </summary>
| p | q |$p \leftrightarrow q$| 
|---|---|---------------------|
| V | V |           V         |
| V | F |           F         |
| F | V |           F         |
| F | F |           V         |

</details>


# 5. Funzioni

$f: A \rightarrow B$ $x \overrightarrow{f} f(x)$:
- A è il dominio di $f$ 
- B è il codominio di $f$
- $f$ è la legge di associazione

> f è la legge d'associazione che associa un elemento nell'insieme A in un insieme B (la funzione è definita dal: dominio,codominio e legge di associazione ($A,B,f$))  
$\forall x \in A, \exists! b \in B : f(x) = b$ 


$f(a)=b$,
b è l'immagine di a tramite $f$

due funzioni sono uguali se e solo se il dominio il codominio e la legge di associazione sono uguali:
<details>
$f: A \rightarrow B \\ f': A'\rightarrow B' \\ \begin{cases} A=A' \\ B=B' \\ f=f'\end{cases}$
</details>

> prioprietà iniettiva (1-1): tutti gli elementi del codominio sono associati a un elemento del codominio diverso
 $f: A \rightarrow B$ se $\forall a \in A,\forall a' \in A : a\neq a' \rightarrow f(a) \neq f(a')$

> l'inniettività dipenda dal dominio

<details>
    <summary>
    esempio
    </summary>

$f(n)=n^2$ non è (1-1) perchè $f(-1)=1=f(1)$  
ma la si può far diventare mettendo come dominio R+

$f(n)=n^3$ è (1-1)
</details>


> surrettiva (su) ogni elemento del codominio deve avere un elemento del dominio per cui f(a)=b
$\forall b \in B, \exists a \in A : f(a)=b$

> la surrettività dipenda dal codominio

<details>
    <summary>
    esempio
    </summary>

$f: A \rightarrow B$  
$f(n)=n^2$ non è (su) perché $\forall b \in B, \nexists a \in A : f(a)=b$  
ma la si può far diventare mettendo come codominio R+

$f(n)=n^3$ è (su)
</details>

> l'immagine di una funzione sono tutti gli elementi di b che sono associati con a

$\text{Img} f = \{ b \in B | \exists a \in A : f(a)=b \}$  
$\text{Img} f \subseteq B$


> Una funzione sia surrettiva che invettiva è detta biunivoca e quindi è invertibile

$f: A \rightarrow B$ è invertibile
$f^{-1}: A \rightarrow B$ e vuol dire che:
- $\forall a \in A: f^{-1}(f(a))=a$  
- $\forall b \in B: f(f^{-1}(b))=b$  

$f$ è ivertibile $\leftrightarrow f$ è biunivoca 

## 5.1. Cardinalità

perchè vengono estesi i numeri razionali a quelli reali

> la cardinalità di un insieme è il numero di elementi di un insieme

due insiemi sono equipotenti solo se i due insiemi hanno la stessa cardinaltà 

due insiemi sono equipotenti se c'è una corrispondenza biunivoca

due insiemi infiniti hanno la stessa cardinalità se hanno una corrispondenza biunivoca

$N$ e $Z$ sono inifiniti
$N \subsetneqq Z$

$N$ e $Z$ sono equipotenti

TODO: esercizio

$f(n)= \begin{cases} n/2 \text{se n è pari} \\ -\frac{n+1}{2} \text{se n è pari} \end{cases}$

## 5.2. Numberailità 

> un insieme è numberabile se esiste una funzione $f : N \rightarrow A$ è biunivoca 

> lemma: è un piccolo teorema

> (Lemma) A è numerabile se è solo se 
$f_1 : A \rightarrow \mathbb{N}$ è surrettiva  
$f_2 : \mathbb{N}\frac{n!}{k!(n - k)!} = \binom{n}{k} = {}^{n}C_{k} = C_{n}^k \rightarrow A$ è surrettiva


si può provare che l'insieme dei numeri razionali è numerabile?

$Q = \{ \frac{n}{m} | n \in N, m \in Z \backslash \{0\}, MCD(n,|m|)=1\}$


# 6. Calcolo Combinatorio

> fattoriale di un numero

> permutazioni: contano l'ordine degli elementi

> combinazioni: contano il numero di set diversi

$n!= 1*2*3*4*5*...*(n-1)*n, n\in \mathbb{N}$ , $0!=1$

il fattoriale si usa per contare le permutazioni di una lista di elementi diversi.

## 6.1. Coefficente Binomiale

$n \in \mathbb{N}, m \in \mathbb{N}$


$\frac{n!}{k!(n - m)!} = \binom{n}{m} = {}^{n}C_{m} = C_{n}^m$

siamo $n,m \in \mathbb{N}: m<=n$, il binomiale riponde quanti sottoinsiemi partendo di m elementi posso formare partendo da un insieme di n(non contano gli ordini,combinazioni).

**Proprietà**:

    
1.  $\binom{n}{k}=\binom{n}{n-k}$
2.  $\binom{n+1}{k}=\binom{n}{k-1}+\binom{n}{k}$

<details>
    <summary>
    Prova coefficiente binomiale
    </summary>

![](img/dimbinomialep1.png)
![](img/dimbinomialep2.png)
</details>

TODO: spiegare il perchè di entrambe le proprietà

## Il binomio di Newton

Come si calcola il binomio $(a+b)^n=?$

TODO: spiegare con parole tue come si calcola il coefficente di ogni binomio

**Formula del binomio di newton**

$(a+b)^n=\displaystyle \sum^{n}_{k=0} \binom{n}{k} a^{n-k}*b^k$

# Teorema di pitagora

dipende dall'assioma che dice che gli angoli del triangolo rettangolo misurano 180°

![](img/teoremadipiagora.png)

# L'insieme dei numeri razionali

Domanda: esistono tanti numeri razinali quanti punti sulla retta, c'p una funzione biunivoca tra Q e i punti di una retta?


$\sqrt{2} \in \mathbb{Q}$

Dimostrazione per assurdo: TODO: da completare