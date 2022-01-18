
# L'insieme dei numeri reali

> $\mathbb{R}$ possiede la proprità di continuità (che manca a $\mathbb{Q}$)
i numeri razionali sono quanti sono i punti della retta? quindi possiamo trovare una funzione biunivoca tra i $\mathbb{Q}$ e i punti sulla retta?.  
Prendiamo il punto $\sqrt{2}$ che è sulla retta, non è rappresentabile con i numeri razionali


<details>
<summary>
Dimostrazione per assurdo
</summary>

Assumiamo $\sqrt{2} \in \mathbb{Q}$ Quindi:  
$\exists m,n \in \mathbb{N} | \sqrt{2} = \frac{m}{n}$

Supponiamo che la frazione sia ridotta ai minimi termini: $MCD(m,n)=1$

$\sqrt{2} = \frac{m}{n}$  
$2 = \frac{m^2}{n^2}$   
$2n^2 = m^2$   

allora $m^2$ è pari quindi $\exists m_1 \in \mathbb{N}: m=2m_1$

$2n^2 = (2m_1)^2$   
$n^2 = 2(m_1)^2$   

$n^2$ è pari ma  $MCD(m,n)=1$ quindi è impossibile
</details>



## 8.1. Teorema radice di n

> Sia $n \in \mathbb{N}$: $n$ non è un quadrato perfetto allora $\sqrt{n} \notin \mathbb{Q}$

<details>
<summary>
dimostrazione
</summary>


Lemma: $m,n,l \in \mathbb{N}$  tali che $MCD(l,m)=1$ allora se $l | m \times n \implies l | n$


supponiamo che $\sqrt{n} \in \mathbb{Q} \implies \exists p,q \in N: \sqrt{n}=\frac{p}{q}$ dove $MCD(p,q)=1$

$n=\frac{p^2}{q^2}$  
$nq^2=p^2$  

essendo che p e q sono primi tra loro allora $p^2$ divide $q^2n$ e quindi dall'lemma $p^2$ divide $n$  

quindi $\exists v \in \mathbb{N}: n = p^2v$

allora riscriviamo $q^2p^2v=p^2$ allora $q^2v=1$

Essendo $q^2 , v \in \mathbb{N}$ allora $v=1$

allora $n=p^2$ n è un quadrato perfetto


</details>

## Intervalli di $\mathbb{R}$


### Intervalli
$[a,b]=\{x \in \mathbb{R} | a \leq n\leq b\}$  
$]a,b[=\{x \in \mathbb{R} | a < n < b\}$  
$[a, \infty [=\{x \in \mathbb{R} | a \le n\}$  


### Maggioranti e Minoranti

> **Insieme Limitato superiormente**   
> $M \in \mathbb{R}$ si dice maggiorante di A se:
> $\forall a \in A$:  $a \leq M$
> se A ammette un maggiorante si dice superiormente limitata

L'insieme dei Maggioranti $M_g(A)=\{x\in R|\forall a \in A, x \geq a\}$

> **Insieme Limitato inferiormente**   
> $\mathbb{m} \in \mathbb{R}$ si dice minorante di A se:
> $\forall a \in A$: $\mathbb{m} \leq a$
> se A ammette un minorante A si dice inferiormente limitato

L'insieme dei Minoranti $M_n(A)=\{x\in R|\forall a \in A, x \leq a\}$

> **Insieme Limitato**  
> se A ammette sia un minorante che un maggiorante è limitato

### Minimo e Massimo di un insieme

> **minimo di un insieme**:  
$\forall a \in A : b \leq a$ (b è i minimo )
> se b è il minimo di A è il più grande dei minoranti

> **massimo di un insieme**:  
> $\forall a \in A : a \leq b$ (b è il massimo)
> se un b è il massimo di A, è il più grande dei maggioranti



### Sup e Inf di un insieme

> se A è superiormente limitato ha il minimo dei maggioranti $\sup A$ ($\sup A$ si chiama estremo superiore di A ), se B non è superiormente limitato  $\sup B= +\infty$

> se A è inferiormente limitato ha il massimo dei minorandi $\inf A$ ($\inf A$ si chiama estremo inferiore  di A)
, se B non è inferiormente limitato  $\inf B= +\infty$ 


Q a differenza di R non ha sempre la proprietà di avere un massimando e un minorando es. $\{q \in \mathbb{Q}| q \le \sqrt{2}\}$

### Esempi

![](../img/minimax.png)

L'intervallo $A = ]3,4]$ :
- Ha come insieme dei massimandi $M_g(A)=\{x \in \mathbb{R}| x \geq 4\}$
- Ha come insieme dei massimandi $M_g(A)=\{x \in \mathbb{R}| x \geq 3\}$
- Ha un massimo 4:$\max A = 4$
- Non ha un minimo: $\nexists \min A$
- $\sup A= 4$
- $\inf A= 3$



## l'insime $\mathbb{R}$

N, Z e Q hanno la stessa cardinalità mentre R ha una cardinalità maggiore $|\mathbb{N}|<|\mathbb{R}|$.

**Dimostrazione per Assurdo**

Supponiamo che esista una funzione:$f:\mathbb{N} \implies [0,1[$ 
definiamo la funzione come:

![](../img/NtoR.png)

allora possiamo crere un numero reale $a \in [0,1[$ tale che $f(n)\neq a \forall n \in \mathbb{N}$

costruiamo a usando un procedimento diagolnale

$r_j=\begin{cases}5 & \text{se } b_{jj}\neq 5 \\ 6 & \text{se } b_{jj}=5\end{cases}$

![](../img/NtoRnot.png)

## Esistenza e uniticità della radice

$\forall a \in \mathbb{R_{+}}, \forall n \in \mathbb{N} /\ \{0\} : \exists! b \in \mathbb{R_{+}} : b^n=a$


**Abuso di notazione**:b si dice radice artimetica n-esima di a e si scrive $\sqrt[n]{a}{:=} b$.

Oss: la radice **aritmetica è un numero $\ge 0$** quindi $\sqrt{4}=2$


**Lemma**:

$\forall n,y \in \mathbb{R}: x,y \ge 0$
si ha:
1. $x^2 \le y^2 \iff x \le  y$
2. $x^2 \ge y^2 \iff x \ge y$
3. $x^2 = y^2 \iff x = y$
4. $x^2 < y \iff \exists \varepsilon > 0: (x+\varepsilon)^2 < y$
5. $x^2 > y \iff \exists \varepsilon > 0: (x+\varepsilon)^2 > y$

le prime tre non valgono solo con x e y alla seconda ma quando condividono qualsiasi stesso esponente.


[dimostrazione](https://virtuale.unibo.it/pluginfile.php/1024181/mod_resource/content/3/11%20Ottobre%202021.pdf)
### Teorema di esistenza di $\sqrt{}$

cosiderando l'insieme $A = \{c \in \mathbb{R} | c \ge 0 , c^2 \le a\}$


TODO:da completare

[dimostrazione pag 13](https://virtuale.unibo.it/pluginfile.php/1024181/mod_resource/content/3/11%20Ottobre%202021.pdf)