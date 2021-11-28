# Sviluppo di serie di Taylor


## Infinitesimo

> IDEA: approssimiamo una funzione ad un polinomio senza cambiare il limite

$f:A\to\mathbb{R}$  
$x_0 \in D(A)$
$f(x)$ si dice **infinitesimo** per $x\to x_o$ se:

$\displaystyle \lim_{x \to x_0} f(x) =0$


### Confronto di infinitesimi

Date due funzioni (infinitesime per $x\to x_0$):
- $f(x)  \xrightarrow{x\to x_0} 0$

- $g(x) \xrightarrow{x \to x_0} 0$


Se esiste:   

$\displaystyle \lim_{x \to x_0} \bigl|\frac{f(x)}{g(x)}\bigr| = L \in \mathbb{R} \cup \{+\infty\}$

allora si hanno i casi:  

1. $L=0$ allora $f(x)$ è un **infinitesimo di ordine superiore** a $g(x)$
2. $0 < L \in \mathbb{R}$ allora $f(x)$ e $g(x)$ sono **infinitesimi equivalenti**
3. $L= +\infty$ o $-\infty$ allora $g(x)$ è un **infinitesimo di ordine superiore** a $f$


<details>
<summary>
Esempi
</summary>

![](vx_images/205564121192423.png)
![](vx_images/18654627283136.png)

</details>

## O piccolo

$f,g: A \to \mathbb{R}, x_0 \in D(A)$  
$f(x)\neq 0$ se $A \backslash \{x_0\}$  
$g(x) \to 0$

Si dice che $\nearrow$ è un o-picolo di $f$ per $x \to x_0$ se :

$\displaystyle \lim_{x \to x_0} \frac{g(x)}{f(x)}=0$ 


In tal caso si scrive: $g(x)=o(f(x))$ per $x \to x_0$

<details>
<summary>
esempi
</summary>

![](vx_images/262344853876896.png)

altri esempi dopo pag 11 [pdf](https://virtuale.unibo.it/pluginfile.php/1078465/mod_resource/content/1/25%20Novembre%202021.pdf)
</details>


### Proprietà degli O-piccoli per x tendente a 0

>Attenzione $x \to 0$ e $(n,m \in \mathbb{N})$

1. $f= o(x^4)\implies f=o(x^m), m<n$
    <details>
    <summary> Dim </summary> 
    
    ![](vx_images/440687388363129.png) </details>

2. $o(x^n)\pm o(x^n)$ è un $o(x^n)$
3. $x^m\times o(x^n)$ è un $o(x^{n+m})$
4. $o(x^n)\times o(x^m)$ è un $o(x^{n+m})$
5. $(o(x^n)^m)$ è un $o(x^{n\times m})$
6. $o(o(x^n))$ è un $o(x^n)$
7. $o(x^n+o(x^m))$ è un $o(x^n), (m\ge n)$ 
8. $o(x^n+d\times x^{n+m})$ è un $o(x^n)$
9. $\frac{o(x^n)}{x^m}$ è un $o(x^{n-m})$ se $m<n$
10. $o(k\times x^n)$ è un $o(x^n)$
11. se $f,g$ sono infinitesime per $x\to x_0$ allora $o(f(x))=o(g(x))$
12. se $h(x)\xrightarrow{x\to 0}k\neq 0 \implies o(h(x)\times x^n)$ è un $o(x^n)$






