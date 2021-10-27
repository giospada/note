

# Successioni Numeriche 
  
successioni di numeri reali è una funzione, perchè essendo una successione devono essere numerati

allora creaiamo $f: \mathbb{N} \rightarrow R$   

$f(0)=a_0$ primo elemento  
$f(1)=a_1$ secondo elmento  
$f(2)=a_2$ terzo elemento  

$\mathbb{N} /\ \{0\} = \mathbb{N^*}$

Esempi:

$a_n = \frac{n}{n+1}, n \in \mathbb{N}$  
$a_n = \frac{(-1)^2}{n+1}, n \in \mathbb{N^*}$  


## Limiti delle successioni


Anche le **successioni posono essere limitate** superiormente o inferiormente o entrabmbi.

<details>
  <summary>
  es
  </summary>

1. $a_n=\frac{1}{n}, n \in \mathbb{N}$  
è limitata  
2. $n \in \mathbb{N} \\ a_n=n^2$   
questa successione è inferiormente limitata ma non superiormente
3. $a_n=(-1)^n*n$  
non è ne inferiormente ne superiormente limitata
</details>


$a_n =\frac{n}{n+1} \rightarrow 1$


### Limiti finiti

$\displaylines{(a_n)_n , L \in \mathbb{R} \text{  si dice che } \displaystyle \lim_{n \rightarrow +\infty} = L \text{ se } \\ \forall \varepsilon >0, \exists \bar{n}=\bar{n} \in \mathbb{N}: \forall n \ge \bar{n} : \\ |a_n -L | < \varepsilon \\ (L - \varepsilon < a_n < L + \varepsilon) \\ (a_n)_n \text{ si dice convergente}}$


<details>
<summary>
Esercizio Limite finito 


</summary>

fissando un $\varepsilon >0$  arbitrario, posso trovare un $\bar{n}$ in modo che :
$\displaylines{\forall n \le \bar{n} \\ |\frac{n-1}{n}-1| < \varepsilon}$ ?



![](vx_images/4562411229295.png)
![](vx_images/48494786818.png)
</details>




### Limiti infiniti

Si dice che $\displaystyle \lim_{n \rightarrow \infty} a_n=+\infty$ se:  
$\displaylines{\forall k > 0,\exists \bar{n}=\bar{n}(k) \in \mathbb{N} : \\ \forall n \ge \bar{n} : a_n \ge k}$  

Si dice che $\displaystyle \lim_{n \rightarrow \infty} a_n=-\infty$ se :  
$\displaylines{\forall k > 0,\exists \bar{n}=\bar{n}(k) \in \mathbb{N} : \\ \forall n \ge \bar{n} : a_n \le -k}$

in questi casi la successione si dice **divergente**



**Oss**: ci sono successioni che non hanno limitie

<details>
  <summary>
  es
  </summary>

$a_n= (-1)^n$
la successione è limitata ma non si avvicina a nessun numero in quanto oscilla

$a_n= (-1)^n\times n$
oscilla e quindi non ha limite
</details>

## Algebra dei limiti

**Teorema** (Algebra dei limiti)

siano $(a_n)_m$,$(b_n)_m$ successioni  tali che, $a_n \rightarrow l_1$ ,$b_n \rightarrow l_1$ dove $l_1,l_2 \in \mathbb{R} \cup \{\infty \} \cup \{\infty\}$

### Somma 

$$a_n+b_n \rightarrow \begin{cases}
l_1+l_2 &\text{se } l_1,l_2 \in \mathbb{R} \\
\infty &\text{se } l_1=+\infty,l_2 \in \mathbb{R}\cup\{+\infty\} \\
-\infty &\text{se } l_1=-\infty,l_2 \in \mathbb{R}\cup\{-\infty\} \\
 \end{cases}$$

Forme Indeterminate $+\infty-\infty$

### Moltiplicazione

$$a_n \times b_n \rightarrow \begin{cases}
l_1\times l_2 &\text{se } l_1,l_2 \in \mathbb{R} \\
+\infty &\text{se } l_1=+\infty,l_2 \in (\mathbb{R}^+\cup\{+\infty\})\backslash \{0\} \\
+\infty &\text{se } l_1=-\infty,l_2 \in (\mathbb{R}^-\cup\{-\infty\})\backslash \{0\} \\
-\infty &\text{se } l_1=+\infty,l_2 \in (\mathbb{R}^-\cup\{-\infty\})\backslash \{0\} \\
-\infty &\text{se } l_1=-\infty,l_2 \in (\mathbb{R}^+\cup\{+\infty\})\backslash \{0\} \\
 \end{cases}$$

Forme Indeterminate $0\times (\pm \infty)$

### Divisione


$$\frac{a_n}{b_n} \rightarrow \begin{cases}
l_1\times l_2 &\text{se } l_1,l_2 \in \mathbb{R} \\
+\infty &\text{se } l_1=+\infty,l_2 \in l_2>0 \\
+\infty &\text{se } l_1=-\infty,l_2 \in l_2<0 \\
-\infty &\text{se } l_1=-\infty,l_2 \in l_2>0 \\
-\infty &\text{se } l_1=+\infty,l_2 \in l_2<0 \\
 \end{cases}$$


Forma Ineterminata:$\frac{\pm \infty}{\pm \infty}$ 

## Le successioni Monotone

$(a_n)_n$ si dice crescente $\forall n \in \mathbb{N}$: $a_n < a_{n+1}$ si scrive $(a_n \nearrow)$

$(b_n)_n$ si dice crescente $\forall n \in \mathbb{N}$: $b_n > b_{n+1}$ si scrive $(a_n\searrow)$

Una successione crescente o descrescente viene chiamata **monotona**


Una **proprietà** importante delle **successioni monotone** è che esse hanno sempre limite, ossia sono **sempre convergenti o divergenti**.

**Teorema**:
se $(a_n)_n$ è crescente, allora $\displaystyle \lim_{n \rightarrow +\infty} a_n = sup \{a_n | n \in \mathbb{N}\}$

se $(a_n)_n$ è descrescente, allora $\displaystyle \lim_{n \rightarrow + \infty} a_n = inf \{a_n | n \in \mathbb{N}\}$
**Dim**:

si tratta di provare che:

$\displaystyle \lim_{n \to +\infty} a_n = sup \{a_n | n \in \mathbb{N}\}$

TODO: da completare


**Crollario**:

$(a_n)_n)$ è crescente e sup limitata **allora**: $(a_n)_n$ è covergente, 
cioè $\exists r \in \mathbb{R}: a_n \rightarrow n $

$(a_n)_n)$ è crescente e inf limitata **allora**: $(a_n)_n$ è covergente, 
cioè $\exists r \in \mathbb{R}: a_n \rightarrow n $

### Il numero e di nepero
 
$a_n = (1+\frac{1}{n}^n), n \in \mathbb{N}^{*}$

$a_1=2$
$a_2=(\frac{3}{2})^2=2,25$
$a_3=(\frac{4}{3})^3=2,370$
$a_4=(\frac{5}{4})^4=2,4414$


Teorema 

$\displaystyle \lim_{n \rightarrow \infty} (1+\frac{1}{n}^n), n \in \mathbb{N}^{*}= e$





