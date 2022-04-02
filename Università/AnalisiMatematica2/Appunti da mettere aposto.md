# 06-Appunti da mettere aposto



## Derivabilità continuità

$f: A \to \mathbb{R}, A \subseteq \mathbb{R}, f$ derivabile in $\bar{x} \in A \implies f$ è continua in $\bar{x}$

Funzione $f: A \to \mathbb{R}$  $A \subseteq \mathbb{R}^2$ aperto $\exists D_x f(\bar{x},\bar{y}), D_y f(\bar{x},\bar{y}) \implies$ continua in $(\bar{x}, \bar{y})$

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


## Curve (cammini) in R^n


- $f: \mathbb{R} \to \mathbb{R}$ (scalari)
- $r:]a,b[ \to \mathbb{R}^n$  (cammini parametrizzati)


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


**Def** $r:]a,b[\to \mathbb{R}^n, r'(t)$= velocità, Se $\exists r''_j(t) \forall j=1,\dots,n$ poniamo $r''(t)=(r''_1(t),\dots,r''_n(t))$ vettore accelerazione



### Derivata lungo una curva (cammino)


Sia $r:]a,b[ \to \mathbb{R}^n, f: \mathbb{R}^n \to \mathbb{R}$  

$(f\cdot r) (t)=f(r(t)),$ r è derivabile in t e f differenziabile in $r(t)$

<details>
<summary>
es
</summary>

$r(t)=(2t,\cos t), f(x,y)=x^2e^{2y}$

$(f \cdot r )(t)= f(r(t))=(2t)^2 e^{2\cos t}$

$D_t (f \cdot r)(t)= 8te^{2\cos t}-8 t^2 \sin t e^{2 \cos t}$

</details>

Torema $r:]a,b[ \to \mathbb{R}^n, f:\mathbb{R}^n\to \mathbb{R}$ differenziale in $r(t)$ e r derivabile in t, allora $(f \cdot r)'(t)=<\nabla f(r(t)),r'(t)>$ $=\sum_{k=1}^n \frac{\delta f}{\delta x_k} (r(t)) r_k'(t)$

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

## Gradiente e Insiemi di livello




