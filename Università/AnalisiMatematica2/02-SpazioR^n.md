# Spazio R^n


Spazio $\mathbb{R}^n=\{x=(x_1,\dots,x_n)|x_1,\dots,x_n \in \mathbb{R} \}$

$\mathbb{R}^1$: retta reale
$\mathbb{R}^2$: piano cartesiano
$\mathbb{R}^2$: spazio ordinario


# Operazioni in R^n

1. somma $x=(x_1,\dots,x_n) \in \mathbb{R}^n$ ,$y=(y_1,\dots,y_n) \in \mathbb{R}^n$ $x+y:=(x_1+y_1, \dots, x_n+y_n)$  
2. moltiplicazione $x=(x_1,\dots,x_n) \in \mathbb{R}^n$ ,$\lambda \in \mathbb{R}^n$ $x\times \lambda:=(\lambda x_1, \dots,\lambda x_n)$  


## Prodotto scalare euclideo in R^n

**Def:** dati $x=(x_1,\dots,x_n) \in \mathbb{R}^n$ ,$y=(y_1,\dots,y_n) \in \mathbb{R}^n$, il prodotto scalare tra x e y **è il numero reale** $<x,y>:=(x_1\times y_1+ \dots+ x_n\times y_n) = \sum^n_{k=1} x_k\times y_k$  (notazione equivalente è $x \cdot y$)


**Proprietà**:
1. simmetrico $<x,y>= <y,x>$  
2. $\forall x,y,z \in \mathbb{R}^n, \forall \lambda,\mu \in \mathbb{R}$ vale $<\lambda x, \mu y, z>= \lambda<x,z>+ \mu <y,z>$
3. $\forall x \in \mathbb{R}^n$ vale  $<x,x> \geq 0$
    - (3 bis) $<x,x>=0 \implies x=\underline{0}$

## Vettori ordtogonali

**Def:** $x,y \in \mathbb{R}^n$ si dice che $x$ e $y$ sono ortogonali $<x,y>=0$

> NOTA:
> Sono ortagonali o quando uno di essi è zero o quando sono perpendicolari


## Norma vettore
**Def:** la norma di un vettore (lunghezza) $x \in \mathbb{R}^n$, $||x||=\sqrt{<x,x>}$

**proprietà**:
1. $\forall x \in \mathbb{R}^n, \lambda \in \mathbb{R}$ vale $|| \lambda x || = |\lambda| \times ||x||$
2.  $||x|| \geq 0, \forall x \in \mathbb{R}^n$  $||x||\leq 0 \iff x=0$
    - disuguaglianza tirangolare $\forall x,y \in \mathbb{R}^n$ $||x+y||\leq ||x||+||y||$



<details>
<summary>
dimostrazione prop 1
</summary>

$\sqrt{<\lambda x,\lambda x>} = \sqrt{\sum^n_{k=1} (\lambda x)^2}=\sqrt{\sum^n_{k=1} \lambda^2  (x)^2}= |\lambda| ||x||$

</details>

<details>
<summary>
visualizzazione disuguaglianza triangolare
</summary>

![](vx_images/94846892889348.png)

</details>


## Normalizzare un vettore

**Normalizzazione**:dato un $x\in \mathbb{R}^n \backslash {\underline{0}}$ cerco un $r>0$ tale che $||rx||=1$ applicando le proprietà 1 della norma del vettore $r=\frac{1}{||x||}$ 

> NOTA:
> con la normalizzazione possiamo scrivere un vettore come il prodotto scalare tra la norma e le sue coordinate polari 

<details>
<summary>
esempio
</summary>

dato un vettore x con un angolo di $\alpha$ è uguale a scrivere $||x||\times(\cos \alpha, \sin \alpha)$
</details>


### Disuguaglianza di couchy- schwarz


$\forall x ,y \in \mathbb{R}^n$ vale $|<x,y>| \leq |x| \times |y|$ vale "=" solo se x,y sono dipendenti


### Disuguaglianza triangolare


$\forall x ,y \in \mathbb{R}^n$ vale $|<x,y>| \leq |x| + |y|$ vale "=" solo se x,y sono dipendenti

<details>
<summary>
dimostrazione
</summary>


$|x+y|^2=|x|^2+|y|^2+2<x,y> \leq |x|^2+|y|^2+2<x,y>$ per la disuguaglianza di cauchy-shwarez
$\le|x|^2+|y|^2+2|x||y|$  ovvero $\leq (|x|+|y|)^2$

</details>



## Formula quadrato di un binomio

Dati $x,y \in \mathbb{R}^n$ $||x+y||^2=<x+y,x+y>=<x,x+y>+<y+x+y>=$ $<x,y>+<x,x>+<y,x>+<y,y>$ $=||x||^2+2<x,y>+||y||^2$



**Def**: dati $x,y \in \mathbb{R}^n$ la distanza tra $x,y$ è il numero della norma della differenza $||x-y||$ 



## Intorni specifici (dischi, palle) 

**def** $x \in \mathbb{R},r >0$  $B(x,r)=\{y \in \mathbb{R}^n / |y-x|<r\}$

 $n=1, x \in \mathbb{R},r >0$  $B(x,r)=\{y \in \mathbb{R}^n / |y-x|<r\}= ]x-r,x+r[$
 
 $n=2, x =(0,0)$  $B((0,0),r)=\{y \in \mathbb{R}^n / |(y_1,y_2)-(0,0)|<r\}= \sqrt{y_1^2+y_2^2}<r$


 $n=2, x =(0,0,0)=\underline{0}$  $B(\underline{0},r)=\{y \in \mathbb{R}^n / |(y_1,y_2)-(0,0)|<r\}= \sqrt{y_1^2+y_2^2}<r$

**Def**: $A \subseteq \mathbb{R}^n$ si dice limitato se $\exists R>0$ tale che $P\subseteq A$


## Insiemi aperti


**Def**: un insieme aperto sia $A \subseteq \mathbb{R}^n$. Si dice che $A$ è aperto se $\forall x \in A, \exists r>o$ tale che $B(x,r)\subseteq A$ 


$n=1 , A=]0,1[=\{x \in \mathbb{R}\space|\space 0<x<1\}$ $]a,b[$ è aperto $\forall a,b \in \mathbb{R}$ $]a,+\infty[$, $]-\infty,b[$ intervalli aperti

## Succcessioni in $\mathbb{R}^n$

una successione in $\mathbb{R}^n$ è una famiglia di $(x_k) k \in \mathbb{N}$ dove $x_k \in \mathbb{R}^n$ $\forall x \in \mathbb{N}5$ $x=(x_k^1,x_k^2,\dots,x_k^n) \in \mathbb{R}^n$ $\forall x \in \mathbb{N}$



**def** successione convergente $(x_k) k \in \mathbb{N}$ successioni in $\mathbb{R}^n, x \in \mathbb{R}^n$ .$\displaystyle \lim_{k \rightarrow \infty}x_k=x$ Si dice $\displaystyle \lim_{k \rightarrow +\infty} x^1_k = x^1 , \dots, \displaystyle \lim_{k \rightarrow +\infty} x^n_k = x^n$


**oss**: $(x_k)_{k \in \mathbb{N}},$ in $\mathbb{R}^n$ $x_k \to x \in \mathbb{R}^n \iff |x_k -x |\to 0$(con k che tende a +infinito)

**Funzioni di più variabili**
$A \subseteq \mathbb{R}^n, B \subseteq \mathbb{R}^q \space n,q \in \mathbb{N}$ $f:A\to B$

$Graf(f)=\{(x,f(x))\in A \times B\}$

Dato $E \subseteq A$,

$Im(E)=\{f(x)|x \in E\}$ 



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


## Derivabilità continuità

$f: A \to \mathbb{R}, A \subseteq \mathbb{R}, f$ derivabile in $\bar{x} \in A \implies f$ è continua in $\bar{x}$

funzione $f: A \to \mathbb{R}$  $A \subseteq \mathbb{R}^2$ aperto $\exists D_x f(\bar{x},\bar{y}), D_y f(\bar{x},\bar{y}) \implies$ continua in $(\bar{x}, \bar{y})$

$f: \mathbb{R}^2 \to \mathbb{R}$

$f(x,y)= \begin{cases} \frac{xy}{x^2+y^2} & \text{se } (x,y)=(0,0) \\ 0 & \text{in } (x,y)=(0,0)\end{cases}$

1. $\exists D_x f(0,0), D_y f(0,0)$ f derivabile
2. f non è continua in (0,0)

$D_x f(0,0)=\displaystyle \lim_{h \rightarrow 0} \frac{f(h,0)-f(0,0)}{h}$

$f(h,0)$ per $h\neq 0$ $=\frac{h\times 0}{h^2+0^2}$ $\forall h \neq 0$

$(h \to f(h,0)$ è $0 \forall h \in \mathbb{R})$

$\displaystyle \lim_{x \rightarrow 0} \frac{0-0}{h}$

Derivabilità differenziabilità


$\mathbb{R}, f:A \to \mathbb{R}$ derivabilie $\displaystyle \lim_{x \rightarrow \infty} \frac{f(\bar{x}+h)-f(\bar{x})}{h}=f'(\bar{x})\in \mathbb{R}$

$\displaystyle \lim_{x \rightarrow \infty} \frac{f(\bar{x}+h)-f(\bar{x})-f'(\bar{x})h}{h}=0$


**Def** $g: \mathbb{R}^2 \to \mathbb{R}, (h,k)\to g(h,k)$

Si dice che $g(h,k)=o(|(h,k)|)$ se vale $\forall \varepsilon >0 \exists \delta_varepsilon >0$ tale che $\frac{|g(h,k)|}{||(h,k)||}<\varepsilon$ se $||(h,k)|| < \delta_\varepsilon$

Dunque $g(h,k)=ah^2+ck^2=o(|(h,k)|)$









