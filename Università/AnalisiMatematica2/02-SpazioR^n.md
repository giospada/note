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

## Formula quadrato di un binomio

Dati $x,y \in \mathbb{R}^n$ $||x+y||^2=<x+y,x+y>=<x,x+y>+<y+x+y>=$ $<x,y>+<x,x>+<y,x>+<y,y>$$=||x||^2+2<x,y>+||y||^2$