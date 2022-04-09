# Matrice Jacobiana e Matrice Hessiana

## Matrice Jacobiana

È un modo per scrivere il gradiente di una funzione quando è in una certa forma.

Data una funzione $f: \mathbb{R}^n \to \mathbb{R}^p$

ossia per esempio $x=(x_1,...,x_n) \to(f_1(x),...,f_p(x))$

Se le p funzioni di arrivo sono differenziabili, allora la matrice jacobiana è definita in questo modo:

$J_f(x) = \begin{pmatrix} \delta_{x_1} f_1(x) & ... & \delta_{x_n} f_1(x)\\ . & . & . \\ \delta_{x_1} f_p(x) & ... & \delta_{x_n} f_p(x) \end{pmatrix}$

Una matrice con p righe e n colonne, che rappresentano **tutte le derivate parziali possibile**

**Osservazione**

Da una funzione differenziabile f(r(x)) in modo simile a quanto fatto prima, abbiamo che 

$J_f(r(t)) J_r(t)$ è uguale al prodotto scalare!

$(\delta_1f(r(t)), ..., \delta_nf(r(t))) \cdot \begin{pmatrix} \delta_{s} r_1(t) \\ . \\ \delta_{s} r_n(t) \end{pmatrix}$

Ossia è proprio $\delta_t(f(r(t))$ il prodotto scalare, ossia $J_{f \cdot r}(t)$ e la cosa bella è che **vale per dimensione qualsiasi**. (vedere gli appunti lezione 11, ci dovrebbe essere l'enunciato di questo).


## Ricerca del massimo e del minimo

> Nota: a differenza delle funzioni a due variabili quando si parla di funzioni a più variabili non possiamo definire il massimo in quanto non abbiamo neanche più il concetto di funzione crescente

sia $f:A \to \mathbb{R}, \bar{x} \in A$ è minimo locale, f è differenziabile in $\bar{x}$, allora si ha che $\nabla f(\bar{x}) = 0$

Quando il gradiente si annulla, quel punto in cui si annulla si chiama **punto critico o stazionario**.

- La stazionarietà non permette di distinguere massimi e minimi (valeva anche per R dim 1


sia $f:A \to \R, \bar{x} \in A$ è minimo locale, f è differenziabile in xbar, allora si ha che $\nabla f(\bar{x}) = 0$

Quando il gradiente si annulla, quel punto in cui si annulla si chiama **punto critico o stazionario**.

- La stazionarietà non permette di distinguere massimi e minimi (valeva anche per R dim 1

## Matrice Hessiana

Questa matrice contiene tutte le derivate seconde possibili per una certa funzione da Rn a R (sarà di dimensione n x n

$$
Hf(x) = \begin{pmatrix}
\delta_{11} f(x) & ... & \delta_{1n} f(x)\\
. & . & . \\
\delta_{n1} f(x) & ... & \delta_{nn} f(x)

\end{pmatrix}
$$

### Teorema di Schwarz !!

Sia f una funzione ben definita, con dominio multidimensionale.

Siano tutte le derivate seconde ben definite.

Allora $\forall ij \in \{1,..,n\}, i \neq j$ si ha che $\delta_{ij}f = \delta_{ji}f$, ossia è un altro modo per dire che la **matrice hessiana è simmetrica**. 

<details>
<summary>
Dimostrazione
</summary>


l'idea principale è utilizzare qualcosa di simile alla differenziabilità per continuità e derivabilità parziale.
    
Considero 

$g(h) = f(x + h, y+h) + f(x, y) - f(x + h,y) - f(x, y + h)$

poi considero 

$u(t) = f(x + t, y+h) + f(x, y) - f(x + t,y) - f(x, y + h)$ e utilizzando lagrange due volte ottengo che 

$g(h) = \delta_{xy}f(x + ah, y + bh)h^2$

Lo faccio ancora per il simmetrico  (cioè costruendomi una funzione v(t) che vari a seconda della y e mi trovo che 

$g(h) = \delta_{yx}f(x + ah, y + bh)h^2$

Faccio il limite per h tendente a 0, dividendo per la stessa variabile, e trovo che sono esattamente uguali.

cioè 

$\lim_{h \to 0} \dfrac{\delta_{yx}f(x + ah, y + bh)h^2}{h^2} = \lim_{h \to 0} \delta_{yx}f(x + ah, y + bh)=  \delta_{yx}f(x,y)$  l'ultimo uguale è giustificabile per la continuità della funzione f (basta aprire e controllare 🙂).

</details>

## Forme quadratiche

Queste cose sembrano essere un buon utilizzo della matrice hessiana. 

Comunque vediamo cosa sono:

prendiamo una matrice $A \in \R^{n \times n}$ tale che sia simmetrica, consideriamo una funzione 

$q_A : \R ^n \to \R$ definita in questo modo : 

$q_A(h) =  \langle Ah, h\rangle$. Scopriremo che c'è una equivalenza (forse isomorfismo) fra un polinomio di grado n e una matrice n per n.

Si può dimostrare che è uguale a una forma quadrata questa matrice, questo perché

$\sum^n_{k,j=1} a_{kj}h_jh_k = \sum^n_{k=1}a_k h^2_k + 2 \sum_{ 1\leq j < k \leq n} a_{jk} h_j h_k$ ed è qualcosa di molto comodo perché questo non è altro che  (ricordando che $a_k$  è un modo semplice per scrivere $a_{kk}$

$$
\langle Ah, h\rangle = (a_1h_1 + ...+ a_nh_n)^2
$$

Ma questo vale nel caso solo in cui $a_ia_k = a_{ik}$, da ricordare!. Comunque c'è questa buonissima corrispondenza e ci piace molto.

### Segno della forma quadratica

**Positivo**

Se per ogni h diverso da zero la forma quadratica è sempre positiva 

esempio se ho solo numeri sulla diagonale, probabilmente è di segno positivo

**Negativo**

Se per ogni h diverso da zero la forma quadratica è sempre negativa

**Indefinita** 

Se esistono due h diversi fra loro per cui la forma della prima è minore di 0, la forma della seconda è maggiore di zero.

**Altro**

Ci sono anche altre caratterizzazione della forma quadratica. 

ad esempio q(h1, h2) = h2^2 non è né indefinita, né positiva questa è **semidefinita**

### Teorema criterio classificazione 2x2

La matrice considerata è sempre 

$\begin{pmatrix} a & b \\ b & c \\ \end{pmatrix}$

**Positivo** 

Una forma quadratica è positiva sse $a > 0 \land ac - b^2 > 0$

**Negativa**

Una forma quadrata è negativa sse  $a < 0 \land ac - b^2 > 0$

**Indefinita**

sse il determinante è negativo., se il determinante è 0 si dice che è una **matrice singolare**. 

    
<details>
<summary>
Dimostrazione
</summary>

vogliamo dimostrare un sse, andiamo per le due frecce.

$\implies$

Se pongo h = (1, 0) ottengo $a > 0$ quindi deve essere così altrimenti assurdo.

se pongo h = (h,1)  (nota questi due h sono diversi) ottengo $ah ^2 + 2bh + c$ che è sempre positivo quando il determinante è negativo, quindi verificato

$\impliedby$

Se $h_2 = 0$ ottengo $ah^2_1 > 0$ vero perché a > 0 e ho un quadrato in R 

Se $h_2 \neq 0$, allora raccogliendo un h2 e ponendo $e = \dfrac{h1}{h2}$, ottengo 

$q(h) = ae^2 + 2be + c > 0$ (già diviso per h2 alla seconda), prendendo il determinante ho che è $b^2 - ac$ , che è sempre minore di 0, quindi sempre vera.

</details>

## Formula di taylor di grado secondo

Sia f di classe $C^2$ su $A\subseteq \mathbb{R}^2$ aperto. Allora per ogni $\bar{x}=(x_1,\dots,x_n)\in A$  vale la formula:

$$
T_2(\bar{x}+h)=f(\bar{x})+<\nabla f(\bar{x}),h> + \frac{1}{2} 
$$

TODO:![](vx_images/569811914268678.png)

## Teorema di classificazione dei punti

**Teorema**: Sia f $A\subseteq \mathbb{R}^2$ aperto $f:A \to \mathbb{R}$, classe $C^2$ sia $\bar{x}\in A$ critico:
- se $Hf(\bar{x})>0\implies \bar{x}$  è minimo locale
- se $Hf(\bar{x})<0\implies \bar{x}$  è massimo locale
- se $Hf(\bar{x})=0\implies \bar{x}$  è di sella


Ricordo che se $A= A^t\in\mathbb{R}^{n\times n}$, $A>0\implies \exists m>0$  tale che $<Ah,h> \ge m|h^2|,\space \fo$



## Funzioni convesse (derivabile)


![](vx_images/243313216268678.png)


In $\mathbb{R}$ la definizione di concava e convessa sono $f''(x)>0,\space \forall x$ 