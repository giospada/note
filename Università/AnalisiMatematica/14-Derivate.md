
# Derivate

## Retta Tangente ad una Funzine

Il procedimento per cercare una retta tangente per un punto x è fissare un punto e per ogni altro punto vicino creare una finchè non si avvicina al punto P.

![](vx_images/4274795830145.png)


Per individuare il coefficente angolare della retta di una delle rette utilizziamo, $y=m(x-x_0)+ f(x_0)$, e il coefficente angolare delal retta r lo troviamo facendo $r_n: y=m_n(x-x_0)+f(x_0) \mbox{ , } m= \displaystyle \lim_{x \to x_0} m_n$

![](vx_images/2007529516787.png)

il coefficiente angolare della tangente sarà $\displaystyle \lim_{x \to x_0} \frac{f(x)-f(x_0)}{x-x_0}$

## Definizione Derivata

> $f: I \to \mathbb{R}$ I intervallo, $x_0 \in I$,$f$ si dice derivabile in $x_0$ se:
> $\exists \displaystyle \lim_{x \to x_0} \frac{f(x)-f(x_0)}{x-x_0}\in \mathbb{R}$   
> in tal caso, tale limite si chiama derivata di f in x_0, e si scrive:  
> $f'(x_0)=\frac{df}{dx}(x_0)=Df(x_0)$

$f$ è derivabile solo se la derivata di destra e di sinistra, esistono e sono uguali $f'_+(x_0)=f'_-(x_0)=f'(x_0)$(derivata a destra è il limite in $x_0^+$ e quella di destra è il limite in $x_0^-$).

Possiamo riscrivere $x$ come $x_0+h$ e trasformare la definizione in $\displaystyle \lim_{h \to 0} \frac{f(x_0+h)-f(x_0)}{h}$



### Equazione Tangente
> Se f è derivabile in $x_0 \in I$ allora esiste una retta tangente al grafico di $f$ in $x=x_0$ ed ha equazione $r: y=f'(x_0)(x-x_0)+f(x_0)$


### Teorema dell'algebra delle derivate

$f,g:I\to \mathbb{R}, x\in I$
$f,g$ sono derivabili in $x_0$, allora:  

|              funzione               |                                      derivata                                      |
| ----------------------------------- | ---------------------------------------------------------------------------------- |
| $f\pm g$ è derivabile in $x_0$      | $(f \pm g)'(x_0)=f'(x_o) \pm g'(x_0)$                                              |
| $f \times g$ è derivabile in $x_0$  | $(f\times g)'(x_0)=f'(x_0)\times g(x_0)+ f(x_0)\times g'(x_0)$                     |
| $\frac{f}{g}$ è derivabile in $x_0$ | $(\frac{f}{g})'(x_0)=\frac{f'(x_0)\times g(x_0)-f(x_0)\times g'(x_0)}{(g(x_0))^2}$ |

### Derivate funzioni coposte

**funzione composta**: $Df(g(x_0))=f'(g(x_0))g'(x_0)$

### Drivate delle Funzioni Goniometriche

**Funzioni Goniometriche**  
1. $D \sin x=\cos x$
2. $D \cos x=-\sin x$
3. $D \tan x= \frac{1}{\cos^2 x}=1+\tan^2 x$

### Derivata Esponenziale

**Esponenziale**
$Da^x=(\ln a)a^x$

### Deriva Logaritmica

**funzione logaritmica**:
$D \log_a y= \frac{1}{\ln a }\times \frac{1}{y}$


## Teorema, deravibilità e continuità

Dato I un intevallo $\subset \mathbb{R}$, $x_0 \in I$,$f: I \to \mathbb{R}$ si ha che:  
se $f$ è derivabile in $x_0 \implies f$   è continua in $x_0$

## Derivate di ordine superiore

> $f: I \to \mathbb{R}$ derivabile su $I \implies \exists f':I \to \mathbb{R}$
Se $f'$ è derivabile in $x_0 \in I : f''(x_0):= \displaystyle \lim_{h \to 0} \frac{f'(x_0+h)-f'(x_0)}{h} \in \mathbb{R}$  


## Classi di derivabilità 


> NOTA  
> la classe di derivabilità denota la regolarità della funzione

$f \in C^k (I) \iff \begin{cases}f \mbox{ è derivabile k-volte su }I_j  \\ f^k\mbox{ è continua su I}\end{cases}$

## Massimo Relativo

> $x_0 \in A$ si dice **punto di massimo relatio** (o locale se)
> $\exists r>0: f(x)\le f(x_0), \forall x \in A \cap I_r(x_0)$

## Minimo Relativo

> $x_0 \in A$ si dice **punto di minimo relatio** (o locale se)
> $\exists r>0: f(x)\ge f(x_0), \forall x \in A \cap I_r(x_0)$


# Teorema di Fermat 

$f:[a,b]\to \mathbb{R}$  

1. $x_0 \in ]a,b[$ punto di massimo o minimo relativo
2. $f$ è derivabile in $x_0$

Allora:  
$f'(x_0)=0$


## Teorema di Rolle

$f:[a,b]\to \mathbb{R}$

1. $f$ è continua su $[a,b]$
2. $f$ è derivabile in $]a,b[$
3. $f(a)=f(b)$

Allora:  
$\exists c \in ]a,b[ : f'(c)=0$

![](vx_images/3176647189382.png)



## Teorema di Lagrnge

$f:[a,b]\to \mathbb{R}$

1. $f$ è continua su $[a,b]$
2. $f$ è derivabile su $]a,b[$

Allora :  
$\exists c \in ]a,b[ : \frac{f(b)-f(a)}{b-a}=f'(c)$

![](vx_images/1352483756905.png)

### Crollairio

$f: ]a,b[ \to \mathbb{R}$
$f$  derivabile t.c. $f'(x)=0,\space \forall x \in ]a,b[$
Allora f è constante

## Teorema di cauchy

$f,g:[a,b] \to \mathbb{R}$

1. $f,g$ continua su  $[a,b]$
2. $f,g$ derivabili su  $]a,b[$
3. $g'(x)\neq 0$ continua su  $\forall x \in ]a,b[$


Allora:
$\exists c \in ]a,b[:\frac{f(b)-f(a)}{g(b)-g(a)}=\frac{f'(c)}{g'(c)}$

## Relazione tra segno della derivata prima e la crescenza della funzine

$f'(x)\ge 0 \mbox{ , }\forall x \in ]a,b[ \iff f$ è crescente su$]a,b[$

$f'(x)> 0 \mbox{ , }\forall x \in ]a,b[ \implies f$ è strettamente crescente su$]a,b[$
9
<details>
<summary>
decresente
</summary>

$f'(x)\le 0 \mbox{ , }\forall x \in ]a,b[ \iff f$ è decrescente su$]a,b[$

$f'(x)< 0 \mbox{ , }\forall x \in ]a,b[ \implies f$ è strettamente decrescente su$]a,b[$

</details>

## Punto minimo e massimo

![](vx_images/4147553139386.png)

> Queste sono le condizioni sufficenti (non necessarie) per il minimo e il massimo






