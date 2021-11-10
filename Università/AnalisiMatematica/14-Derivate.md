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

### Derivate funzioni coposte

**funzione composta**:
$Df(g(x_0))=f'(g(x_0))g'(x_0)$

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

