---
header-includes: |
            \usepackage{mathtools}
---

# Esempi di Dimostrazioni

## Teorema di pitagora

dipende dall'assioma che dice che gli angoli del triangolo rettangolo misurano 180°

![](../img/teoremadipiagora.png)


$Area(ABCD)=(a+b)^2$  
$Area(EFGH)=c^2$  
$Area(ABCD)-Area(EFGH)=4*\frac{ab}{2}$  


$(a+b)^2-c^2=4\frac{ab}{2}$
$a^2+b^2+2ab-c^2=2ab$
$a^2+b^2-c^2=0$
$a^2+b^2=c^2$



## teorema di Euclide (Numeri primi)

Quanti sono i nueri primi?

Dimostrazione per assurdo, supponiamo che i numueri primi siano finiti, possiamo elencarli in ordine crescente:

$1<p_1<p_2<p_3<...<p_n$


Creiamo un numero $m {:=} p_1\times p_2 \times ... \times p_n +1$, essendo che m è più grande di tutti i numeri primi in particolare più grande di $p_n$ non dovrebbe essere un numero primo, quindi può essere diviso da un numero primo.

Se $m$ fosse divisibile per $p_1$ allora $\exists m_1 \in \mathbb{N}: m_1 \times p_1=m=p_1\times p_2 \times ... \times p_n +1$    
$m_1\times p_1 -( p_1\times p_2 \times ... \times p_n )=1$  
$p_1 (m_1 - p_2 \times ... \times p_n )=1$  
$p_1 (m_1 - p_1\times p_2 \times ... \times p_n )=1$  
quindi: $p_1 =1$  

essendo che $m$ non è divisibile per nessuno primo, $m$ è primo.

