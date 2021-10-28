# 13-Teorema degli Zeri

Se abbiamo una funzione continua che in un certo punto è negativa e in un altro è positiva sappiamo che la funzione ha al minimo un punto in cui si annulla.


Lemma: 
$(b_n)_n \subset \mathbb{R}$
$b_n < 0 \forall n (b_n > 0 \forall n)$
$\displaystyle \lim_{x \rightarrow \infty} b_n= l \in \mathbb{R} \implies l \le 0$


![](vx_images/3549954881665.png)




$f: [a,b] \to \mathbb{R}$ continua  $f(a)\times f(b) <0 \implies \exists c \in ]a,b[: f(c)=0$


per trovare il punto in cui passa da zero utilizziamo questo algoritmo.
$f(a)<0$ e $f(b)>0$ costruiamo due successioni $(a_b)_n$, $(b_n)_n$

prendiamo il punto medio $\frac{(a+b)}{2}$ possiamo avere tre casi:

1. $f(\frac{a_n+b_n}{2}) = 0$  fine 
2. $f(\frac{a_n+b_n}{2}) < 0$ $a_{n+1}=\frac{a_n+b_n}{2}, b_{n+1}=b_n$
3. $f(\frac{a_n+b_n}{2}) > 0$ $b_{n+1}=\frac{a_n+b_n}{2}, a_{n+1}=a_n$
