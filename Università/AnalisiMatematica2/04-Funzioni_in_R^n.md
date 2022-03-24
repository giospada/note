# Funzioni in R^n

## Insiemi aperti


**Def**: un insieme aperto sia $A \subseteq \mathbb{R}^n$. Si dice che $A$ è aperto se $\forall x \in A, \exists r>o$ tale che $B(x,r)\subseteq A$ 


$n=1 , A=]0,1[=\{x \in \mathbb{R}\space|\space 0<x<1\}$ $]a,b[$ è aperto $\forall a,b \in \mathbb{R}$ $]a,+\infty[$, $]-\infty,b[$ intervalli aperti

## Succcessioni in $\mathbb{R}^n$

Una successione in $\mathbb{R}^n$ è una famiglia di $(x_k) k \in \mathbb{N}$ dove $x_k \in \mathbb{R}^n$ $\forall x \in \mathbb{N}5$ $x=(x_k^1,x_k^2,\dots,x_k^n) \in \mathbb{R}^n$ $\forall x \in \mathbb{N}$


### Successione convergente
**Def** successione convergente $(x_k) k \in \mathbb{N}$ successioni in $\mathbb{R}^n, x \in \mathbb{R}^n$ .$\displaystyle \lim_{k \rightarrow \infty}x_k=x$ Si dice $\displaystyle \lim_{k \rightarrow +\infty} x^1_k = x^1 , \dots, \displaystyle \lim_{k \rightarrow +\infty} x^n_k = x^n$


**oss**: $(x_k)_{k \in \mathbb{N}},$ in $\mathbb{R}^n$ $x_k \to x \in \mathbb{R}^n \iff |x_k -x |\to 0$(con k che tende a +infinito)

## Funzioni di più variabili 
 
$A \subseteq \mathbb{R}^n, B \subseteq \mathbb{R}^q \space n,q \in \mathbb{N}$ , Data$f:A\to B$ il grafico è $Graf(f)=\{(x,f(x))\in A \times B\}$



Funzioni Scalarei 
- $q=1, A\subset \mathbb{R}^n , f:A \to \mathbb{R}$
- $n=1, q>1 I \subseteq \mathbb{R}, f:I \to \mathbb{R}^q$

**Def**(funzione continua) $A \subseteq \mathbb{R}^n, B\subset \mathbb{R}^q$  $f: A \to B$ Sia $\bar{x} \in A$ si dice f continua in $\bar{x}$ se $\forall (x_k)_{k \in \mathbb{N}}$ $\begin{cases}x_k \in A  \forall k \\ x_k \to \bar{x} \end{cases}$ vale $f(x_k) \to f(\bar{x})$  $k\to + \infty$ (convergenza in $\mathbb{R}^q$) 

Si dimostra che tutte le funzioni "elementari" sono continue

**oss** $f:A\to B$ è continua in $\bar{x}$ $\iff \forall \varepsilon  >0 \exists \delta_{\varepsilon}$ tale che $|f(y)-f(\bar{x})| < \varepsilon$ $\forall x \in A$ con $|y-\bar{x}|<\delta$


Si dimostra che se  $f_1,f_2,\dots,f_p:\mathbb{R}^n\to \mathbb{R}$ scalari sono continue, allora ogni insieme $A=\{x\in\mathbb{R}|f(x)_1<c_1,\dots,f(x)_p<c_p\}$






## Funzione radicale

$f: \mathbb{R}^2 \to  \mathbb{R}$ tale che $\exists g:[0; +\infty[ \to \mathbb{R}$ per cui $f(x,y)=g(|(x,y)|)=g(\sqrt{x^2+y^2})$



## Insiemi di livello

gli insiemi di livello sono un modo di rappresentare le funzioni che consiste nel studiare una funzione ad  un livello minore, per esempio studiare una funzione in $\mathbb{R}^3$ come diverse funzioni in $\mathbb{R}^2$


<details>
<summary>
es
</summary>


$f:\mathbb{R}^2 \to \mathbb{R}$
$A \subseteq \mathbb{R}^2, f:A \to \mathbb{R}, b \in \mathbb{R}$ l'insieme di livello b di f è $L_b=\{(x,y)\in A | f(x,y)=b\}=f(b)$

</details>



## Funzioni di primo grado

$f: \mathbb{R}^2 \to \mathbb{R},\space f(x,y)= ax+by+c \space (a,b,c)\in \mathbb{R}^3$ 

il $Graf(f)$ è un piano 

## Derivata parziale

$A \subseteq \mathbb{R}^2$

$f:A \to \mathbb{R}$

$\frac{\delta f}{\delta x}(\bar{x},\bar{y})=\displaystyle \lim_{h \rightarrow 0} \frac{f(\bar{x}+h,\bar{y})-f(\bar{x},\bar{y})}{h}$

Se il limite esiste si chiama derivata parziale di f rispetto a x  ( nel punto $(\bar{x},\bar{y})$)


$\frac{\delta f}{\delta y}(\bar{x},\bar{y})=\displaystyle \lim_{k \rightarrow 0} \frac{f(\bar{x},\bar{y}+k)-f(\bar{x},\bar{y})}{k}$


<details>
<summary>
Notazioni
</summary>

$\frac{\delta f}{\delta y}f(\bar{x},\bar{y})= D_y f(\bar{x},\bar{y})=\delta_y f(\bar{x},\bar{y})$

</details>

$f(x,y)=x^3+y+2e^{-2y}$

Se $\exists D_x f$ in $(\bar{x},\bar{y})$ scrivo $\nabla f(\bar{x},\bar{y})=(D_x f(\bar{x},\bar{y}), D_y f(\bar{x},\bar{y}))$

Se $\exists D_x f$ e $D_y f$ in ogni $(x,y) \in Dom(f)$, poniamo $\nabla f(x,y)= (D_xf(x,y), D_y f(x,y))$
$\nabla f : Dom(f) \mathbb{R}^2\to \mathbb{R}^2$

$f(x,y)= xye^{-x^2}$ $D_x f= y D_x(xe^{-x^2})$
$=y[e^{-x^2}-2x^2 e^{-x^2}]=y(1-2x^2)e^{-x^2}$

$D_y f= xe^{-x^2}$ 

-----


Caso n dimensionale


$\mathbb{R}^n$ 

$e_1=(1,0,\dots,0)$
$e_1=(0,1,\dots,0)$

$f:\mathbb{R}^n \to \mathbb{R}$

$x=(x_1,x_2,\dots,x_n) \to_f f(x)$

$D_{x_j} (\bar{x})=x+he_j=(x_1,\dots,x_n)+(0,\dots,h_j,\dots,0)=(x_1,\dots,x_j+h_j,\dots,x_n)$

$D_{x_j}=\displaystyle \lim_{x \rightarrow \infty} \frac{f(\bar{x}+he_j)-f(\bar{x})}{h}$