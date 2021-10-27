
# Limiti Funzioni


> Intorno sferico di un punto $x_0 \in \mathbb{R}$ di raggio r


$x_0 \in \mathbb{R}$, $r \in \mathbb{R}: r>0$

si dice **interno (sferico)** di centro $x_0$ e raggio r:

$I_r(x_0) = \{x\in \mathbb{R} : |x-x_1|<r\}$

$I_r=]x_0-r,x_0+r[$


> Punto di accumulazione  di un insieme

$A\subset \mathbb{R}$  
$\bar{x}\in\mathbb{R}$ si dice **punto di accumulazione** di a se:  

$x_0\in\mathbb{R}\ \mbox{è di accumulazione per }E\subseteq\mathbb{R}\\ \\ \mbox{ se }\forall\varepsilon>0\ \exists y\in E,\ y\neq x_0\mbox{ t.c. }y\in B(x_0,\varepsilon)$

$a \cap (I_r(\bar{x})\backslash \{\bar{x}\})\neq \emptyset$

![](vx_images/1189241576710.png =254x)

$D(A)=\{\bar{x}\in \mathbb{R}| \bar{x}\text{è di accomulazione per A}\}$

**Idea**:$\bar{x}$ si dice punto di accumulazione di A se ci si può avvicinare arbitrariamente a $\bar{x}$, rimanendo in A!

<details>
<summary>
esempio
</summary>
![](vx_images/2412763123188.png =539x)
</details>



**proposizione**:

$A \subset \mathbb{R}$, $\bar{x} \in \mathbb{R}$, $\bar{x}$ è di accumulazione per A _se e solo se_: $\exists (a_n)_n \subseteq A \mbox{ t.c.:}$

1. $a_n \neq \bar{x} \forall n$
1. $a_n \xrightarrow{n\to \infty} \bar{x}$

### Limite

## Limiti Notevoli


### Sin

$\displaystyle \lim_{x \rightarrow 0} \frac{\sin x}{x}=1$

TODO:dimostrazione

### Cos 

$\displaystyle \lim_{x \rightarrow 0} \frac{1-\cos^2 x}{x^2}=\frac{1}{2}$

TODO:dimostrazione


### Esponenziale
$\displaystyle \lim_{x \rightarrow 0} \frac{a^x-1}{x}=\ln a$ con 

## Definizione di limite finito


$f: A \rightarrow \mathbb{R}, x_0 \in D(A)$
si dice che $\displaystyle \lim_{x \rightarrow x_0}  f(x)=+\infty(-\infty)$se:  $\displaylines{\forall M \in \mathbb{R} \exists \delta = \delta(x_o,M)>0 \\ \forall x \in A : 0 < |x-x_0| < \delta \\ \implies f(x)> M}$


## Limite Finito da Destra e Sinistra

$\displaystyle \lim_{x \rightarrow x_0^+}f(x)=l \iff \displaylines{\forall \varepsilon \in \mathbb{R} \exists \delta = \delta(x_o,\varepsilon)>0 \\ \forall x \in A : x_0  < x <x_0+ \delta \\ \implies |f(x) -l|< \varepsilon }$


$\displaystyle \lim_{x \rightarrow x_0^-}f(x)=l \iff \displaylines{\forall \varepsilon \in \mathbb{R} \exists \delta = \delta(x_o,\varepsilon)<0 \\ \forall x \in A : x_0-\delta  < x <x_0 \\ \implies |f(x) -l|< \varepsilon }$

## Limite Infinito  da Destra e Sinistra

TODO: completare


## Definizione Limite 

$$\displaystyle \lim_{x \rightarrow x_0} L=
\begin{cases} 
    \exists \displaystyle{\lim_{x \rightarrow x_0^-}f(x)}, \displaystyle{\lim_{x \rightarrow x_0^+}f(x)}\\ 
    \displaystyle{\lim_{x \rightarrow x_0^-}f(x)}=\displaystyle{\lim_{x \rightarrow x_0^+}f(x)}=L 
\end{cases}$$


## Limite Infinito

$$\lim_{x\to +\infty} f(x) = \begin{cases}
l \iff |f(x) - l| < \epsilon \\
+\infty \\
- \infty
\end{cases}$$


$\displaylines{\forall \varepsilon, \exists \delta) \delta(\varepsilon) > 0 : \forall x \in A : x < - \delta \\ \implies \begin{cases} |f(n)-l| < \varepsilon \\ f(n) > \varepsilon \\ f(n)< - \varepsilon  \end{cases}}$

### Area Del Cerchio


 Sia C un cerchio di raggio $r$, $S_n£ èpoligono regolare instritto di n lati instritto nel cerchio:
 
 ![](vx_images/1575947139296.png)
 
si calcola l'area di questo poligono con il numero di lati che tende ad infinito.


$A(C)=\displaystyle \lim_{x \rightarrow \infty} A(S_n)$



![](vx_images/999333696819.png)
<details>
<summary>
dimostrazione
</summary>


![](vx_images/5423044485911.png)
![](vx_images/4461069811662.png)

</details>