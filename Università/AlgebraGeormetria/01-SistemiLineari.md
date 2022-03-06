# SistemiLineari

Un sistema lineare è un insieme di equazioni lineare che devonno essere soddisfatte contemporaneamente


<details>
<summary>
esempio
</summary>

$\begin{cases} 3x -2y =1 \\x+y=7\end{cases}$

in questo caso si può rappresentare come due rette sul piano cartesiamo ed esiste solo la soluzione $(3,4)$

</details>

Il sistema potrebbe non avere soluzioni come infinite

Due sistemi lineari si dicono **equivalenti** se hanno le stesse soluzioni.

##  Equazione lineare


un equzione lineare è un equazione del tipo: $a_1x_1+a_2x_2 +\dots + a_nx_n=b \text{ dove } a_1,\dots, a_n,b \in \mathbb{R}$
gli $a_i$ sono i coefficenti e b è il termine noto


<details>
<summary>
proprità delle equazioni
</summary>

- aggiungendo ad entrambi i membri uno stesso numero l'uguaglianza rimane
- moltiplicando ad entrambi i membri uno stesso numero l'uguaglianza rimane

</details>

## Soluzioni dei sistemi lineari

una soluzione è una n-upla ordinata (n numeri ) che sostituiti alle incognite rendono vere l'uguaglianza



## Matrici

Una matrice $n\times m$ con coefficenti in $\mathbb{R}$ è una tabella con n righe e m colonne

l'insieme di matrici $m\times n$ si indica con $M_{m,n} (\mathbb{R})$ se $m=n$ allora la matrice si dice quadrata $M_{n,n}(\mathbb{R})=M_{n}(\mathbb{R})$, se $A\in M_{m,n}(\mathbb{R})$ scriviamo anche $A(a_{i,j}) \text{ dove } i=1..m \text{ e } j=1..n$ 


### Vettori

una matrice con  1xn si dice **vettore riga**

una matrice con  nx1 si dice **vettore colonna**


### Somma 

siano $A,B \in M_{n,n}(\mathbb{R})$ definiamo $C=A+B$ se $A=(a_{i,j}),B=(b_{i,j}),C=(a_{i,j}) \text{ allora la somma è definita come }c_{i,j}=a_{i,j}+b_{i,j}$


<details>
<summary>
esempio
</summary>

$$
\begin{pmatrix} 1 & 0 & -1 \\ 3 & -5 & 1\end{pmatrix} + \begin{pmatrix} -1 & 2 & -1 \\ 1 & 7 & -2\end{pmatrix} = \begin{pmatrix} 0 & 2 & -2 \\ 4 & 2 & -1\end{pmatrix}
$$
</details>


### Prodotto tra vettori

Primo esempio tra un vettore riga e un vettore colonna della stessa lunghezza . (se $A\in M_{1,m}(\mathbb{R}),B\in M_{m,1}(\mathbb{R})$) il risultato è un numero ($AB \in \mathbb{R}$) 
<details>
<summary>
come si calcola 
</summary>

$$
c_{i,j}=\begin{pmatrix} a_{i1} & a_{i2} & ... & a_{im}\end{pmatrix}\begin{pmatrix} b_{1j} \\ b_{2j} \\ ... \\ b_{mj}\end{pmatrix}=a_{i1}b_{1j}+a_{i2}b_{2j}+...+a_{im}b_{mj}
$$

forma compatta

$$
c_{ij}= \sum_{\substack{h=1}}^{s}a_{ih}b_{hj}
$$

</details>





### Prodotto Matrici



se $A\in M_{m,r}(\mathbb{R}),B\in M_{r,n}(\mathbb{R})$) il risultato è un numero $AB=C, C\in M_{m,n}\mathbb{R}$ e si calcola ${\displaystyle c_{ij}=\sum _{r=1}^{r}a_{ir}b_{rj}}$

il prodotto righe per colonne di due matrici è **definito** solo se il numero di righe della prima è uguale al numero di colonne della seconda, e anche se è definito non gode della proprietà commutativa

<details>
<summary>
esempio
</summary>

$$
A=\begin{pmatrix} 1 & 0 & 3 & -1 \\ 0 & -2 & 2 & 1 \\ 1 & 0 & -1 & 0\end{pmatrix} \space B= \begin{pmatrix} 0 & 1 \\ -3 & 5 \\ 1 & 0 \\ 2 & -1\end{pmatrix}
$$

si ha $c_{12}=(1*1)+(0*5)+(3*0)+(-1*-1)=2$

e $c_{31}=(1*0)+(0*-3)+(-1*1)+(0*2)=-1$

$$
C=\begin{pmatrix} 1 & 0 & 3 & -1 \\ 0 & -2 & 2 & 1 \\ 1 & 0 & -1 & 0\end{pmatrix} \begin{pmatrix} 0 & 1 \\ -3 & 5 \\ 1 & 0 \\ 2 & -1\end{pmatrix}= \begin{pmatrix} 1 & 2 \\ 10 & -11 \\-1&1\end{pmatrix}
$$

</details>

#### Proprità matrici

- **Proprità associativa** (se è definitio il prodotto) $A(BC)=(AB)C$    
- **Proprità distributiva** $A(B+C)=AB+AC$  

- **Non vale** commutativa



### Trasposizione

se $A$ è una matrice con $m,n$ righe e colonne la sua trasposta $A^t$ è la matrice $M_{n,m}(\mathbb{R})$ ottenuta da $A$ scambiando righe e colonne


quindi $(A^t)_{i,j}=A_{ji}$


## Matrici e Sistemi Lineari


consideriamo un sistema lineare della forma

$$
\begin{cases}a_{11}x_1 + a_{21}x_2 + ... +a_{n1} x_n = b1\\a_{12}x_1 + a_{22}x_2 + ... +a_{n2} x_n = b2\\...\\a_{1m}x_1 + a_{2m}x_2 + ... +a_{nm} x_n = b_m\end{cases}
$$

possiamo scrivere questo sistema nel seguente modo

$$
\begin{pmatrix}a_{11}x_1 + a_{21}x_2 + ... +a_{n1} x_n \\a_{12}x_1 + a_{22}x_2 + ... +a_{n2} x_n\\...\\a_{1m}x_1 + a_{2m}x_2 + ... +a_{nm} x_n \end{pmatrix}=\begin{pmatrix} b_1\\b_2\\...\\b_m\end{pmatrix}
$$

quindi il sistema può essere riscritto utilizzando il prodotto righe per colonne

$$
\begin{pmatrix}a_{11} & a_{21}& ... &a_{n1} \\a_{12} & a_{22} & ... &a_{n2} \\...\\a_{1m} & a_{2m} & ... &a_{nm} \end{pmatrix}\begin{pmatrix} x_1\\x_2\\...\\x_m\end{pmatrix}=\begin{pmatrix} b_1\\b_2\\...\\b_m\end{pmatrix}
$$

o più semplicemente come $A_{\underline x}=\underline b$


<details>
<summary>
un altra forma compatta
</summary>

$$
A(a|b)=\begin{pmatrix}a_{11} & a_{21}& ... &a_{n1} & |& b_{1} \\a_{12} & a_{22} & ... &a_{n2}  & | & b_2\\ \vdots &\vdots && \vdots & | & \vdots \\a_{1m} & a_{2m} & ... &a_{nm} & | &b_n \end{pmatrix}
$$

</details>

dove $A=(a_{ij})$ è la matrice $m \times n$ dei coefficienti delle incognite$\underline x =\begin{pmatrix} x_1\\x_2\\...\\x_m\end{pmatrix}$ è la colonna delle $n$ incognite, e $\underline b = \begin{pmatrix} b_1\\b_2\\...\\b_m\end{pmatrix}$ è la colonna degli $m$ termini noti.


## Matrice Scala

una matrice si dice in forma a scala se sono soddisfatte le seguenti condizioni

1. eventuali righe nulle si trovano in fondo alla matrice;
2. il primo elemento non nullo di ogni riga (non nulla) si trova più a destra del primo elemento non nullo della riga precedente
    
<details>
<summary>
esempio
</summary>


$$
    A=\begin{pmatrix}1 & -1&-1&2&-4\\0&0&-1&3&5\\0&0&0&\frac{1}{3}&1\\0&0&0&0&0\end{pmatrix}
$$

</details>

### Pivot e Rango righe
**Pivot**: primo elemento non nullo di una riga 

**Rango righe** numero delle righe non nulle $rr(A)$

<details>
<summary>
esempio
</summary>

$$
A=\begin{pmatrix}1 & -1&-1&2&-4\\0&0&-1&3&5\\0&0&0&\frac{1}{3}&1\\0&0&0&0&0\end{pmatrix}
$$

i pivot di A sono $1,-1,\frac{1}{3}$ quindi $rr(A)=3$

</details>

### Risolvere sistemi con matrici a scala

Un sistema lineare associato ad una matrice a scala, si risolve faccilmente ( se ha soluzione ) per sostituzione dal basso e ricavando le incognite corrispondenti ai pivot, se una variabile non è una pivot la lasciamo generica



<details>
<summary>
esempio
</summary>
il sistema può essere risolto per sostituzioni successive dal basso, cioè a partire dall'ultima equazione e risalendo verso la prima:

dalla quarta equazione abbiamo $x_4=1$

sostituendo $x_4=1$ nella terza equazione abbiamo $x_3=x_4=1$

sostituendo $x_3=1$ nella seconda equazione abbiamo $x_2=2+2x_3=4$

sostituendo $x2=4$ nella prima equazione abbiamo $x_1=\frac 14 (1-2x_2-3x_3-4x_4)=-\frac 73$

il sistema ha dunque una sola soluzione $(\frac 72,4,1,1)$.

nota: nel caso

$$
(A|\underline b) = \begin{pmatrix}4&2&3&4&|&1\\0&1&-2&0&|&2\\0&0&1&-1&|&2\end{pmatrix}
$$

 arriveremo a $x_1=\frac 14(-3-11x_4)$ , che indica un sistema con infinite soluzioni in quella forma.

</details>

### Algoritmo di Gauss

Strategia: dato un sistema lineare tramite l'algritmo di Gauss lo trasformiramo in un sistema lineare a scala che è equivalente.

1. se $a_{11}=0$ si scambiano la prima riga di A con una riga il cui elemento non è nullo, e lo indichiamo con a.
2. per ogni riga oltre la prima, se il primo elemento è nullo non facciamo nienete, se il primo elemento non è nullo lo chiamiamo $b$ e sostituiamo la riga corrente con la rpima riga moltiplicata per $-\frac{b}{a}$
3. Tutti gli elementi della prima colonna sono nulli (tranne il pvot), dunque si considera la matrice cancellando la prima riga e la prima colonna e si torna al punto 1



#### Proprietà


Ci sono 3 operazioni dette operazioni elementari, che non cambiano le soluzioni di un sistema:

1. scambio di due equazioni, cioè lo scabio di due rige nella matrice
2. moltiplicazione di un'equazione per un numero reale diverso da 0
3. sostituzione dell'equazione i-esima e della j-esima moltiplicata per un numero reale $\alpha$ qualsiasi.q


## Verificare è risolvibile

bisogna fare il check se il rango righe della matrice dei coefficenti è uguale alla matrice completa, per esempio data una matrice A bisogna verificare se il $rr(A)=rr(A|b)$

Per capire qunte soluzioni ci sono devo contare il numero di pivot confontare al numero di righe, se c'è una riga nulla implica che ci sia una variabile libera e quindi infinte soluzioni




## Sistema omogeneo


Un sistema si dice omogeneo, quando tutti i valori noti sono zero $\implies$ che ci sia sempre una soluzione


<details>
<summary>
esercizio
</summary>

discutere al variare di $\alpha$ le soluzioni del seguente sistema lineare omogeneo associato alla matrice

$$
\begin{pmatrix}
\alpha &  3\alpha & \alpha & |& 0 \\
\alpha+1 & 3\alpha -2 & \alpha & |& 0  \\
2\alpha & 4\alpha  & \alpha+1  & |& 0 \\
\end{pmatrix}
$$

risolvi



</details>



