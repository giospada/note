# De Hopital

## Lemmi Introduttivi

$h: A \to R, \bar{x}\in D(a):$ allora $(l \in \mathbb{R} \cup \{+\infty\} \cup \{-\infty\})$  

1. $\displaystyle \lim_{x \to \bar{x}?^-} h(x)=l \iff \begin{cases} \forall (x_n)_n \subseteq A, x_n < \bar{x} , \forall n \mbox{ tale che: } x_n \to \bar{x} \\ \mbox{si ha:} h(x_n) \to l  \end{cases}$
2. $\displaystyle \lim_{x \to \bar{x}^+} h(x)=l \iff \begin{cases} \forall (x_n)_n \subseteq A, x_n > \bar{x} , \forall n \mbox{ tale che: } x_n \to \bar{x} \\ \mbox{si ha:} h(x_n) \to l  \end{cases}$
3. $\displaystyle \lim_{x \to \bar{x}} h(x)=l \iff \begin{cases} \forall (x_n)_n \subseteq A, x_n \neq \bar{x} , \forall n \mbox{ tale che: } x_n \to \bar{x} \\ \mbox{si ha:} h(x_n) \to l  \end{cases}$

## Teorema di de l'Hopital


Siano $f,g: [a,b]\to \mathbb{R}$ due funzioni reali di variabile reale continue in $[a,b]$ e derivabili in $(a,b)$ eccetto al più $x_0$, con $-\infty \le a< b \le +\infty$; sia $g'(x)$ diversa da 0 per $x\neq x_0$ 

$\lim_{x\to x_0}{|f(x)|} = \lim_{x\to x_0}{|g(x)|} = \infty$
$\lim_{x\to x_0}{f(x)} = \lim_{x\to x_0}g(x) = 0$
$\lim_{x \to x_0}{\frac{f'(x)}{g'(x)}} = L \in \mathbb{\bar{R}}$
$\lim_{x \to x_0}{\frac{f(x)}{g(x)}} = L$

## Dimostrazioni
