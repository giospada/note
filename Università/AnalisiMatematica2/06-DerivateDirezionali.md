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

<details>
<summary>
es
</summary>

$f(x,y)=xe^{xy}\space (\bar{x},\bar{y}) = (2,0), v=(v_1,v_2)$
$\frac{\delta f}{\delta v}(1,0), g(t)=f(2+tv_1,tv_2)=(2+tv_1)e^{(2tv_2+t^2v_1v_2)}$ 


$g'(t)=e^{(2tv_2+t^2v_1v_2)}+(2tv_2+t^2v_1v_2)+(2+tv_1)(2v_2+2tv_1v_2)$

$g'(0)=v_1+4v_2=v_1+4v_2$

</details>


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

<details>
<summary>
es
</summary>


$f(x_1,x_2,x_3)=ln(x_1^2+x_2x_3^2)$

$\bar{x}=(-1,2,-1)$

calcolare 
$\frac{\delta f}{\delta v}(\bar{x})$ $\nabla(x)$ $=(\frac{2x_1}{x_1^2+x_2x_3^2},\frac{x_3^2}{x_1^2+x_2x_3^2},\frac{2x_2x_3}{x_1^2+x_2x_3^2})$ $=(\frac{-1}{3},\frac{1}{3},\frac{-4}{3})$

Dunque

$\frac{\delta f}{\delta v}=<(\frac{-1}{3},\frac{1}{3},\frac{-4}{3}),v>$




</details>



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

</details>


<details>
<summary>
esempio
</summary>

$f(x,y)=\sin(x^2+y^2)$

$(a,b)=(3,4)$
cerco $v_\max$  

$\nabla f(x,y)=(2x\cos(x^2+y^2),2y\cos(x^2+y^2))$ $=2\cos(x^2+y^2)(x,y)$
$=2\cos(x^2+y^2)(x,y)$ 
$\nabla f(3,4)=2\cos(25)\space(3,4)$

$v_\max=\frac{\nabla f(3,4)}{|\nabla f(3,4)|}$ $=\frac{3,4}{|(3,4)|}$ $=\frac{(3,4)}{\sqrt{25}}=(\frac{3}{5},\frac{4}{5})$ 

</details>


<details>
<summary>
es
</summary>

$f(x,y)=e^{xy^3}$

$\nabla f(x,y)=(y^3e^{xy^3},3xy^2e^{xy^3})$

$\nabla f(2,-1)=(-e^{-2},6e^{-2})$

$v_\max=\frac{(-1,6)}{|(-1,6)|}=(\frac{-1}{\sqrt{37}},\frac{6}{\sqrt{37}})$

$\frac{\delta f}{\delta v_\max}(2,-1)=|\nabla f(2,-1)|=$ $e^{-2}|(-1,6)|=e^{-2}\sqrt{37}$

</details>


## Curve (cammini) in R^n


- **scalari** $f: \mathbb{R}^n \to \mathbb{R}$
- **cammini parametrizzati**$r:]a,b[ \to \mathbb{R}^n$, con $]a,b[ \subseteq \mathbb{R}$


considero $r:]a,b[ \to \mathbb{R}^n$  
$]a,b[ \to t \to r(t)=(r_1(t),\dots , r_n(t))\in \mathbb{R}^n$

<details>
<summary>
es
</summary>

$r(t)=(\cos t,\sin t)$

data una funzione $h: \mathbb{R}\to \mathbb{R}$ 

allora  il grafico della funzione è uguale al grafico di $r(t)=(t,h(t))$


cammino a elica $r(t)=(\cos t, \sin t ,t) \in \mathbb{R}^3$

</details>


**Def**: (Velocità di un cammino) $r:]a,b[ \to \mathbb{R}^n$ $(r(t)=(r_1(t),\dots,r_n(t)))$.    
Sia $t \in [a,b]$ . Se le funzioni $r_1,\dots,r_n$ sono derivabili in t si dice che r è derivabile in t e si pone $r'(t)=(r'_1(t),\dots,r'_1(t))=$ velocità di $r$ al tempo t.


<details>
<summary>
es
</summary>


$r(t)= x+tv=(x_1+tv_1,\dots,x_n+tv_n)$  
$r'(t)=(v_1,\dots,v_n)=v$ (constante in t)

$r(t)= x+t^3v=(x_1+t^3v_1,\dots,x_n+t^3v_n)$  

$g'(t)=3t^2v \in$ span $\{ v\}, \forall t$  dipendente da t

</details>

**Def**: (velocitò scalare di $r:]a,b[\to \mathbb{R}^n$)  Se r è derivabile in $t\in ]a,b[, r'(t)$ velocità, $|r'(t)|=$ velocità scalare


<details>
<summary>
es
</summary>

$r(t)=(\cos t,\sin t),\space r'(t)=(-\sin t,\cos t)$


</details>


## Derivate funzioni composte

Sia $r:]a,b[ \to \mathbb{R}^n$  derivabile in $t \in ]a,b[$

$$
\begin{cases}
r_1(t+s)= r_1(t)+r'_1(t)s+o(s), s\to 0 \\
\vdots \\
r_n(t+s)= r_n(t)+r'_n(t)s+o(s), s\to 0
\end{cases}
$$

$o(s)= (o_1(s),\dots, o_n(s))$  
$r(t+s)-r(t)=r'(t)s+o(s)$

$\displaystyle \lim_{s \rightarrow 0} \frac{|O(s)|}{s}=0$

<details>
<summary>
es
</summary>
(curva singolare)

$r(t)=(t^3,t^2)$

$r'(t)=(3t^2,2t) \space \forall t \in \mathbb{R}$

$r'(0)=(0,0)$  $t=0$ punto singolare


$r(t)=(t^3,t^2)$  se $t^3=s$ allora $g(s)=(s,|s|^{\frac{2}{3}})$  (è una curva con lo stesso percorso di r)

</details>


**Def** $r:]a,b[\to \mathbb{R}^n, r'(t)$= velocità, Se $\exists r''_j(t)\space \space \forall j=1,\dots,n$ poniamo $r''(t)=(r''_1(t),\dots,r''_n(t))$ vettore accelerazione



### Derivata lungo una curva (cammino)


**Teorema:**Sia $r:]a,b[ \to \mathbb{R}^n, f: \mathbb{R}^n \to \mathbb{R}$  

$(f\cdot r) (t)=f(r(t)),$ r è derivabile in t e f differenziabile in $r(t)$ allora $(f \cdot r )'(t)=< \nabla f(r(t)), r'(t)>$


<details>
<summary>
Generealizzazione del teorema
</summary>

Torema $r:]a,b[ \to \mathbb{R}^n, f:\mathbb{R}^n\to \mathbb{R}$ differenziale in $r(t)$ e r derivabile in t, allora $(f \cdot r)'(t)=<\nabla f(r(t)),r'(t)>$ $=\sum_{k=1}^n \frac{\delta f}{\delta x_k} (r(t)) r_k'(t)$

</details>

<details>
<summary>
es
</summary>

$r(t)=(2t,\cos t), f(x,y)=x^2e^{2y}$

$(f \cdot r )(t)= f(r(t))=(2t)^2 e^{2\cos t}$

$D_t (f \cdot r)(t)= 8te^{2\cos t}-8 t^2 \sin t e^{2 \cos t}$

</details>

<details>
<summary>
es
</summary>

$r(t) = (2t,\cos t), f(x,y)=x^2 e^{2y}$ $\nabla f(x,y)=(2xe^{2y},2x^2 e^{2y})$

$r'(t)=(2,-\sin t)$  
$(f \cdot r)'(t)=< \nabla f(2t,\cos t),(2,-\sin t)>$
$=< (2 * 2t e^{2\cos t},2(2t)^2e^{2\cos t}),(2,-\sin t)>$
$=8t e^{2\cos t}-8\sin(t)t^2e^{2\cos t}$

</details>
