
# Limiti Funzioni


## Intorno Serico e Punto di accomulazione
> Intorno sferico di un punto $x_0 \in \mathbb{R}$, e raggio $r \in \mathbb{R}: r>0$ 
> $I_r(x_0) = \{x\in \mathbb{R} : |x-x_1|<r\}$
> $I_r=]x_0-r,x_0+r[$


> $\bar{x}$ è **Punto di accumulazione** di un insieme A, $A\subset \mathbb{R}$, $\bar{x}\in\mathbb{R}$ se:  
> 
> $\displaylines{\forall r > 0 : \\ a \cap (I_r(\bar{x})\backslash \{\bar{x}\})\neq \emptyset}$

![](vx_images/1189241576710.png =254x)

$D(A)=\{\bar{x}\in \mathbb{R}| \bar{x} \mbox{ è di accomulazione per A}\}$

**Idea**:$\bar{x}$ si dice punto di accumulazione di A se ci si può avvicinare arbitrariamente a $\bar{x}$, rimanendo in A!

<details>
<summary>
esempio
</summary>

![](vx_images/2412763123188.png =539x)
</details>



**proposizione**:

$A \subset \mathbb{R}$, $\bar{x} \in \mathbb{R}$, $\bar{x}$ è di accumulazione per A _se e solo se_: $\exists (a_n)_n \subseteq A \mbox{ t.c.:}$

1. $\forall n \mbox{ , } a_n \neq \bar{x}$
1. $a_n \xrightarrow{n\to \infty} \bar{x}$



## Definizione di limite finito


$f: A \rightarrow \mathbb{R}, x_0 \in D(A)$
si dice che $\displaystyle \lim_{x \to x_0}  f(x)=L$se:
$\displaylines{\forall \varepsilon \in \mathbb{R}\mbox{ , }  \exists \delta = \delta(x_o,\varepsilon)>0: \forall x \in A  : \\ 0 < |x-x_0| < \delta  \implies |f(x)-L|> \varepsilon}$


<details>
<summary>
Visualizzazione del limite
</summary>

![](vx_images/5320002239302.png)
</details>


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

## Limiti Notevoli


### Sin

$\displaystyle \lim_{x \rightarrow 0} \frac{\sin x}{x}=1$

TODO:dimostrazione

### Cos

$\displaystyle \lim_{x \rightarrow 0} \frac{1-\cos^2 x}{x^2}=\frac{1}{2}$

TODO:dimostrazione


### Esponenziale
$\displaystyle \lim_{x \rightarrow 0} \frac{a^x-1}{x}=\ln a$ con 



## Esercizi sui limiti


$\displaystyle \lim_{x \rightarrow -1} \frac{3x+2}{2x^2+4x+2}$

<details>
<summary>
Soluzione
</summary>
![](vx_images/1800508746822.png)
</details>


$\displaystyle \lim_{x \rightarrow \infty} \frac{x^2+x-2}{x^2+3x}$

<details>
<summary>
soluzione
</summary>


![](vx_images/1957820535914.png)

</details>

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


## Gerarchia degli infiniti

tutte queste funzioni tendono ad infinito, ma non tutte tendono con la stessa forza:

1. $log_a x$ con $(a>1)$
2. $\sqrt[n]{x}$ 
3. $\displaystyle \sum^n_{j=0} a_j x^j$ con $a_n>0$
4. $a^x \mbox{ con } (a> 1)$
5. $x^x$

per esempio:

$$\displaylines{f(x) \to +\infty \\ 
g(x) \to \infty \\ }$$
$$\displaylines{
 \displaystyle \lim \frac{f(x)}{g(x)}} = \begin{cases}
 0 & \mbox{se g(x) cresce più velocemente} \\
 +\infty & \mbox{se f(x) cresce più velocemente} \\
 \end{cases}
 
$$



###  Funzioni continue

> punto isolado di un insime
> $A \subset \mathbb{R}, x_0 \in A$ se $x_0$ si deice punto isolato di A se $x_0 \notin D(A)$ ( $x_0$ non è un punto di accomulazione)


> funzione continua in $x_0$
> $f:A \to \mathbb{R}$
> $x_0 \in A$

$f$ si dice **continua in $x_0$** se:
1. $x_0 \notin D(A)$ cioè $x_0$ è un punto isolato di A
2. $x_0 \in D(A) \implies \displaystyle \lim_{x \rightarrow \infty} f(x)=f(x_0)$


##### Algerba tra le funzioni continue

date f e g due cunzioni continue allora:

1. $f \pm g$ è continua in $x_0$
2. $\displaylines{c \in \mathbb{R} & cf(x)}$ è continua in $x_0$
3. $f \times g$ è continua in $x_0$
3. $\frac{f}{g}$ è continua in $x_0$ ( se$ $g(x_0)\neq 0$)
4. $|f|$ è continua in $x_0$ 

### Esempio importante

per esempio

$f(x)=\begin{cases}x^2 & \text{se} & x\neq 0\\ 2 & \text{se } & x=0\end{cases}$

## Composto

$g \circ  f= g(f(x))$ 

f è continua in $x_0$, e g è continua in $f(x_0)$ allora: 
$g \circ f: x \to g(f(x))$ è continua in $x_0$

