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
