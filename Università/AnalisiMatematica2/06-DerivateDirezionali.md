# Derivate Direzionali

<details>
<summary>
retta parametrica
</summary>

$\mathbb{R}^n,x \in \mathbb{R}^n, v \in \mathbb{R}^n\backslash \{0\}$,  $\{x+tv|t\in \mathbb{R}\}$, questo insieme è una retta parametrica passate per x e parallela a $v$

</details>


## Derivata direzionale

> è una generalizzazione di una derivata parziale

**Def** $A\in\mathbb{R}^2$, $f:A\to\mathbb{R}$, $(\bar{x},\bar{y}) \in A$ $v=(v_1,v_2)$ vettore unitario ($|v|=1$) la derivata direzionale $\frac{\delta f}{\delta v}(\bar{x},\bar{y})$ è definita dal seguente limite $\displaystyle \lim_{t \rightarrow 0} \frac{f((\bar{x},\bar{y})+t(v_1,v_2))-f(\bar{x},\bar{y})}{t}=$ $\frac{\delta f}{\delta v}(\bar{x},\bar{y})=D_vf(\bar{x},\bar{y})$

**Oss 1**: $v=e_1=(1,0)$, $\implies \frac{\delta f}{\delta e_1}=\frac{\delta f}{\delta x}$ , (Analogamente se $v=e_2 \implies$ $\frac{\delta f}{\delta e_1}=\frac{\delta f}{\delta x}$)


**Oss 2** $g(x)=f(\bar{x}+tv_1,\bar{y}+tv_2)$,  $g'(0)=\displaystyle \lim_{t \to 0} \frac{g(t)-g(0)}{t} =$ $\displaystyle \lim_{t \rightarrow 0} \frac{f(\bar{x}+tv_1,\bar{y}+tv_2)-f(\bar{x},\bar{y})}{t}$ $= \frac{\delta f}{\delta v}(\bar{x},\bar{y})$




### Formula del gradiente

**Teorema** $A \in \mathbb{R}^2, f: A \to \mathbb{R}$  f differenziabile in $(\bar{x},\bar{y}) \in A$ alora $\forall v \in \mathbb{R}^2, |v|=1$ vale $\frac{\delta f}{\delta v}(\bar{x},\bar{y})=<\nabla f(\bar{x},\bar{y}), (v_1,v_2)>$ in particolare osservo linearità in $(v_1,v_2)$

$\nabla f(\bar{x},\bar{y})=(D_x f(\bar{x},\bar{y}),D_y f(\bar{x},\bar{y}))$

<details>
<summary>
es
</summary>

$f(x,y)=e^{x^2+y^2}$
$v=(a,b)=(2,1)$


$\nabla f(x,b)=(2xe^{x^2+y^2}, 2ye^{x^2+y^2})=$ $2e^{x^2+y^2}(x,y)$

$\nabla f(2,1)= 2e^5 (2,1)$


$\frac{\delta f}{\delta v}(2,1)= < \nabla f(2,1),(v_1,v_2)>=<2e^5(2,1),(v_1,v_2)>=4e^5v_1+2e^5v_2$



</details>

<details>
<summary>
dimostrazione
</summary>

$\displaystyle \lim_{t \rightarrow 0} \frac{f((a,b)+tv)-f(a,b)}{t}=< \nabla f(a,b) , (v_1,v_2)>$

$f((a,b)+tv)-f(a,b)=<\nabla f(x,b), tv> + o(||tv||)$


$\displaystyle \lim_{t \rightarrow 0} \frac{<\nabla f(a,b),tv> +o(t)}{t}=<\nabla f(a,b),v>$
$\displaystyle \lim_{t \rightarrow 0} <\nabla f(a,b),v> +\frac{o(t)}{t}$


</details>

Tutto vale in $\mathbb{R}^n, x(x_1,\dots,v_n)$ $f:A\to \mathbb{R}$ $A \subseteq \mathbb{R}^n$ aperto f differenziale $\bar{x} \in A$ allora

$\frac{\delta f}{\delta v}(\bar{x})=<\nabla f(\bar{x}),v>=\sum_{k=1}^n\frac{\delta f}{\delta v}(\bar{x})v_k$




## Direzione max crescita


> **Problama**: $A \subseteq \mathbb{R}^2, (a,b)\in A$, $f: A \to \mathbb{R}$ differenziali. cerchiamo tra tuttele direzioni unitarie $v \in \mathbb{R}^2$ quella che rende max


**Steps**(trovare il vettore di crescita massima):  

Sia una funzione $f A \to \mathbb{R}$  differenziabile in $(a,b)$, cerchiamo una scelta di $v \in \mathbb{R}^2, |v|=1$ che renda massima la derivata $\frac{\delta f}{\delta v} (a,b)$. 

Essendo f differenziabile utilizziamo il gradiente: $\nabla f (a,b)$
- se è uguale a $0$ va bene $\forall v$ tc $|v|=1$
- se è diverso continuiamo a cercarlo

La scelta di $\max_{|v|=1}\frac{\delta f}{\delta v}(a,b)=<\nabla f(a,b), \frac{\nabla f(a,b)}{|\nabla f(a,b)|}>$

è la derivata del vettore è di $f$ con il vettore massimo è $|\nabla f(a,b)|$




<details>
<summary>
passaggi per arrivare alla formula
</summary>

Uno Teorema prec. $\frac{\delta f}{\delta v}(a,b)=<\nabla f(a,b),(v_1,v_2)>$

Se $\nabla f(a,b)=0 \implies$ $\frac{\delta f}{\delta v}=0 \forall v$

Se $\nabla f(a,b)\neq0 \implies$ Scriviamo $\nabla f(a,b)=|\nabla f(a,b)| \frac{\nabla f(a,b)}{|\nabla f(a,b)|}=$ $r(\cos \mu,\sin \mu)$

$r>0$ opporiamo, $\mu \in [0,2\mu]$ Analogamente scrivo $(\cos \theta, \sin \theta)$ per $\theta \in [0,2\pi]$ $<\nabla f(a,b),b>=<r(\cos \mu,\sin \mu),(\cos\theta,\sin \theta)>=(\cos \mu \cos \theta+ \sin \mu \sin \theta)=r \cos (\mu - \theta)$

Dueque la derivata  $\frac{\delta f}{\delta v}(a,b)$ è massima se $(\cos \theta,\sin \theta)$ è un multimplo $>0$ di $\nabla f(a,b)$ dunque $v_\max=\frac{\nabla f(a,b)}{|\nabla f(a,b)|}$



**Sintsi**

f diff in $(a,b), \nabla f(a,b)\neq 0$   
$\max \frac{\delta f}{\delta v}(a,b)=$ $\frac{\delta f}{\delta v_\max}(a,b)$

$v_\max=\frac{\nabla f(a,b)}{|\nabla f(a,b)|}$ .Infine $\frac{\delta f}{\delta v_\max} <\nabla f(a,b),v_\max>=$ $<\nabla f(a,b), \frac{\nabla f(a,y)}{|\nabla f(a,b)|}=\frac{1}{|\nabla f|} <\nabla f,\nabla f>$ $= \frac{|\nabla f|^2}{|\nabla f|}= |\nabla f(a,b)|=\frac{\delta f}{\delta v_\max}(a,b)$

$f((a,b)+\varepsilon v_\max)-f(a,b) \approx \varepsilon|\nabla f(a,b)|$

