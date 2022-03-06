# Analisi delle Ricorsioni


## Metodo dell'iterazione

**Idea**: sostituiamo iterativamente la parte ricorsiva nell’equazione finchè non appare uno schema ricorsivo legato al passo di iterazione

<details>
<summary>
esempio
</summary>

![](vx_images/163812216268499.png)

</details>

## Metodo di sostituzione


1. Ipotizzare la soluzione
2. Usare l'induzione matematica per dimostrare la ricorsione

Ovviamante si può utilizzare solo se si ha un'ipotesi da verificare

<details>
<summary>
esempio
</summary>

![](vx_images/64852598826022.png)

</details>


## Albero di ricorsione

In un albero di ricorsione un nodo esprime il costo di un sottoproblema  

> Idea: può essere visto come la versione su albero del metodo iterativo

1 Generiamo l’albero di ricorsione dall’equazione di ricorrenza
2 Calcoliamo il numero di nodi ad ogni livello dell’albero
3 Identifichiamo qualche schema ricorrente legato al livello
dell’albero

Può essere complesso formulare un’ipotesi (metodo della sostituzione)
L’albero di ricorsione pu`o essere usato per generare ipotesi
Tali ipotesi possono poi essere validate col metodo di sostituzione



## Teorema dell'esperto

$$
T(n)= \begin{cases}d & & \text{if }n=1\\aT(n/b)+cn^\beta & &\text{if }n>1\end{cases} 
$$

e sia $\alpha = \frac{\log a} {\log b}$. l'equazione di ricorrenza ha la seguente soluzione:

1. $T(n)=\Theta(n^\alpha) \text{ if }\alpha > \beta$
2. $T(n)=\Theta(n^\alpha\log n) \text{ if }\alpha = \beta$
3. $T(n)=\Theta(n^\beta ) \text{ if }\alpha < \beta$
    
    
<details>
<summary>
applicazione
</summary>

$$
T(n)= \begin{cases}d & & \text{if }n=1\\aT(n/b)+cn^\beta & &\text{if }n>1\end{cases} 
$$

1. nel caso della ricerca binaria, abbiamo $T(n)=T(n/2)+O(1).$ da cui $a=1, b=2,\beta=0$; siamo nel secondo caso in quanto $\alpha = \frac{\log 1}{\log 2}=0$ e $\beta = 0$, da cui $T(n)=\Theta(\log n)$.
2. consideriamo $T(n)=16T(n/4)+n$; in questo caso $a=16, b=4 \text{ e }\beta=1$. siamo nel primo caso in quanto $\alpha = \frac{\log 16}{\log 4}=\frac42=2 \text{ e }\beta=1$, da cui $T(n)=\Theta(n^2)$
3. consideriamo $T(n)=2T(n/2)+n^2$; in questo caso $a=2, b=2 \text{ e }\beta=2$. siamo nel terzo caso in quanto $\alpha = \frac{\log 2}{\log 2}=1 \text{ e }\beta=2$, da cui $T(n)=\Theta(n^2)$

il teorema fondamentale non si può applicare ad algoritmi ricorsivi che non effettuano partizioni bilanciate.

ad esempio, selection sort (cerca il minimo, scambia con il primo elemento, e procedi ricorsivamente sul resto del vettore) ha equazione di ricorrenza del tipo

$$
T(n)=\Bigg\lbrace  \begin{matrix}1\\n+T(n-1)\end{matrix}\quad \frac{\text{if }n=1}{\text{if }n>1}
$$

come altro esempio, il calcolo di fibonacci ricorsivo ha equazione di ricorrenza del tipo

$$
T(n)=\Bigg\lbrace  \begin{matrix}1\\T(n-1)+T(n-2)+1\end{matrix}\quad \frac{\text{if }n\le1}{\text{if }n>2}
$$

in questi casi utilizzeremo altre tecniche per risolvere le equazioni di ricorrenza.
    
-
</details>