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


## Scrittura compatta

un sistema lineare si può scrivere in maniera compatta con le matrici

<details>
<summary>
es
</summary>


da 
$\begin{cases} 3x -2y =1 \\x+y=7\end{cases}$

a 

$\begin{matrix} 3 & -2 &| 1 \\1 &1 & |7\end{matrix}$
</details>

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



se $A\in M_{m,r}(\mathbb{R}),B\in M_{r,n}(\mathbb{R})$) il risultato è un numero $AB=C, C\in M_{m,n}\mathbb{R}$ e si calcola ${\displaystyle c_{ij}=\sum _{r=1}^{n}a_{ir}b_{rj}}$

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
