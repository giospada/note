

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

Anche le successioni posono essere limitate superiormente o inferiormente o entrabmbi.

es:
TODO:aggiungere

$a_n =\frac{n}{n+1} \rightarrow 1$

## Limiti 

### Limiti finiti

$(a_n)_m , L \in \mathbb{R} \text{  si dice che } \lim_{n \rightarrow \inf} = L$ se $\forall e >0, $

in questo  caso la funzione si dice **convergente**
TODO: da completare



### Limiti infiniti

Si dice che $\displaystyle \lim_{n \rightarrow \infty} a_n=+\infty$ se $\forall k > 0,\exists \bar{n}=\bar{n}(k) \in \mathbb{N} : \forall n \ge \bar{n} : a_n \ge k$

Si dice che $\displaystyle \lim_{n \rightarrow \infty} a_n=-\infty$ se $\forall k > 0,\exists \bar{n}=\bar{n}(k) \in \mathbb{N} : \forall n \ge \bar{n} : a_n \le -k$

in questi casi la successione si dice **divergente**

TODO: aggiungere esempi

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

**Teorema** (Algebra dei limiti)

$(a_n)_m$,$(b_n)_m$ successioni  

$a_n \rightarrow l_1$ ,$b_n \rightarrow l_1$
dove $l_1,l_2 \in \mathbb{R} \cup \{\infty \} \cup \{\infty\}$

allora:

$a_n+b_n \rightarrow \begin{cases} l_1+l_2 se l_1,l_2 \in \mathbb{R} \\ +\infty se l_1 =  \end{cases}$

TODO:copiare la somma delle serie e idotto 7-8

$0 +(\pm \infinity)$ indefinito
$0 \times(pm \infty)$ indefinito
$\fract{(\pm \infty)}{\pm \infty}$ indefinito

### Le successioni Monotone

(a_n)_n si dice crescente $\gorall n \in \mathbb{N}$: $a_n \le a_{n+1}$

(b_n)_n si dice crescente $\gorall n \in \mathbb{N}$: $b_n \ge b_{n+1}$

Una successione crescente o descrescente viene chiamata **monotona**


Una proprietà importante delle successioni monotone è che esse hanno sempre limite, ossia sono sempre convergenti o descrescenti.

**Teorema**:
se $(a_n)_n$ è crescente, allora $\displaystyle \lim_{n \righarrow +\infty a_n = sup \{a_n | n \in \mathbb{N}\}$

se $(a_n)_n$ è descrescente, allora $\displaystyle \lim_{n \rightarrow + \infty} a_n = inf \{a_n | n \in \mathbb{N}\}$
**Dim**:

si tratta di provare che:

$\displaystyle \lim_{n \righarrow +\infty a_n = sup \{a_n | n \in \mathbb{N}\}$

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





