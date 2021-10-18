
# L'insieme dei numeri reali

i numeri razionali sono quanti sono i punti della retta? quindi possiamo trovare una funzione biunivoca tra i $\mathbb{Q}$ e i punti sulla retta?.

Prendiamo il punto $\sqrt{2}$ che è sulla retta, è rappresentabile con i numeri razionali


**Dimostrazione per assurdo**: 

Assumiamo $\sqrt{2} \in \mathbb{Q}$ Quindi:  
$\exists m,n \in \mathbb{N} | \sqrt{2} = \frac{m}{n}$

Supponiamo che la frazione sia ridotta ai minimi termini: $MCD(m,n)=1$

$\sqrt{2} = \frac{m}{n}$  
$2 = \frac{m^2}{n^2}$   
$2n^2 = m^2$   

allora $m^2$ è pari quindi $\exist m_1 \in \mathbb{N}: m=2m_1$

$2n^2 = (2m_1)^2$   
$n^2 = 2(m_1)^2$   

$n^2$ è pari ma  $MCD(m,n)=1$ quindi è impossibile



TODO: aggiugere dimostrazione per un numero $\sqrt{n}$ \in $\mathbb{Q}$

## Intervalli di $\mathbb{R}$


### Intervalli
$[a,b]=\{x \in \mathbb{R} | a \leq n\leq b\}$  
$]a,b[=\{x \in \mathbb{R} | a \le n\le b\}$  
$[a, \infty [=\{x \in \mathbb{R} | a \le n\}$  


### Ineismi Limitati
**Insieme Limitato superiormente**   
$M \in \mathbb{R}$ si dice maggiorante di A se:
$\forall a \in A$:  $M \leq a$

> se A ammette un maggiorante si dice superiormente limitata

**Insieme Limitato inferiormente**   
$\mathbb{m} \in \mathbb{R}$ si dice minorante di A se:
$\forall a \in A$: a \leq $\mathbb{m}  $

> se A ammette un minorante A si dice inferiormente limitato

**Insieme Limitato**  
> se A ammette sia un minorante che un maggiorante è limitato

### Minimo Massimo di un insieme
**minimo di un insieme**:  
$\forall a \in A : b \leq A$ (b è i minimo )

**massimo di un insieme**:  
$\forall a \in A : a \leq b$ (b è il massimo)

![](../img/minimax.png)

Per esmpio $]3,4]$ ha un massimo ma non un minimo


se un a il minimo è il più grande dei minoranti

se un a il massimo è il più grande dei maggioranti


se A è superiormente limitato ha il minimo dei maggioranti $\sup A$, se B non è superiormente limitato  $\sup B= +\infty$

se A è inferiormente limitato ha il massimo dei minorandi $\inf A$, se B non è inferiormente limitato  $\inf B= +\infty$


Q a differenza di R non ha sempre la proprietà di avere un massimando e un minorando es. $\{q \in \mathbb{Q}| q \le \sqrt{2}\}$


## l'insime $\mathbb{R}$

N, Z e Q hanno la stessa cardinalità mentre R ha una cardinalità maggiore $|\mathbb{N}|<|\mathbb{R}|$.

**Dimostrazione per Assurdo**

Supponiamo che esista una funzione:$f:\mathbb{N} \Rightarrow [0,1[$ 
definiamo la funzione come:

![](../img/NtoR.png)

allora possiamo crere un numero reale $a \in [0,1[$ tale che $f(n)\neq a \forall n \in \mathbb{N}$

costruiamo a usando un procedimento diagolnale

$r_j=\begin{cases}5 & \text{se } b_{jj}\neq 5 \\ 6 & \text{se } b_{jj}=5\end{cases}$

![](../img/NtoRnot.png)

## Esistenza e uniticità della radice

$\forall a \in \mathbb{R_{+}}, \forall n \in \mathbb{N} /\ \{0\} : \exists! b \in \mathbb{R_{+}} : b^n=a$


**Abuso di notazione**:b si dice radice artimetica n-esima di a e si scrive $\sqrt{a}^{n}\coloneqq b$.

Oss: la radice **aritmetica è un numero $\ge 0$** quindi $\sqrt{4}=2$

TODO: ricopiare il lemma pag 5

**Lemma**:

$\forall n,y \in \mathbb{R}: x,y \ge 0$
si ha:
1. $x^2 \le y^2 \Leftrightarrow x \le  y$
2. $x^2 \ge y^2 \Leftrightarrow x \ge y$
3. $x^2 = y^2 \Leftrightarrow x = y$

TODO: mandcano le ultime

### Teorema di esistenza di $\sqrt{}$

cosiderando l'insieme $A = \{c \in \mathbb{R} | c \ge 0 , c^2 \le a\}$
