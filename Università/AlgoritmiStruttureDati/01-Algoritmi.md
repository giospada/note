# Algoritmi

> Procedura per risolvere un problema prendendo determinati input e dando determinati output in un numero finito di passi

##  Analizzare gli algoritmi

dobbiamo analizzare :
- la quanità di memoria
- il tempo d'esecuzione di un algoritmo


![](vx_images/572822910268496.png)


### Theta


La notazione theta indica $f \in \Theta(g)$ indica che le due funzioni f e g hanno la stessa crescita 

$\Theta(g(n)) = \{f(n) : \text{ esistono delle costanti positive c1, c2 e n0 tali che } 0 ≤ c_1g(n) ≤ f(n) ≤ c_2g(n) \text{ per ogni } n ≥ n_0\}$


### O grande


Limite asintotico superiore, $f\in O(g)$ incica che la funzione g ha una crescita minore uguale a quella di g

$O(g(n)) = \{f(n) : \text{esistono delle costanti positive c e n0 tali che } 0 ≤ f(n) ≤ cg(n) \forall n ≥ n_0\}$

### Omega

Limite asintotico inferiore, $f\in \Omega(g)$ f è omega di g se f ha una crescita maggiore uguale a g


$\Omega(g(n)) = \{f(n) : \text{esistono delle costanti positive c e n0 tali che } 0 ≤ cg(n) ≤ f(n) per ogni n ≥ n_0\}$


### Teorema di theta


$\forall f(n) ,g(n) : f(n) = Θ(g(n)) \iff f(n) = O(g(n)) \wedge f(n) = \Omega(g(n))$

### O piccolo


Limite asintotico inferiore stretto, indica una funzione con crescita strettamente minore

$o(g(n)) = \{f(n) : \text{per qualsiasi costante c > 0, esiste una costante n0 > 0 tale che  } 0 ≤ f(n) < cg(n) \forall n ≥ n0\}$

oppure
$\displaystyle \lim_{x \rightarrow +\infty} \frac{f(x)}{g(x)}=0$


###  omega piccola

Limite asintotico maggiore stretto, indica una funzione che ha una crescita maggiore

$\omega(g(n)) = \{f(n) : \text{per qualsiasi costante c > 0, esiste una costante n0 > 0 tale che  }     cg(n) <  f(n), \forall n ≥ n0\}$


## Proprietà della notazione asintotica

### Transitiva


$f (n) = O(g(n)) \wedge g(n) = O(h(n)) \implies f (n) = O(h(n))$

Vale anche per $o,\omega,\Theta,\Omega$


### Riflessiva

$f(n)=O(f(n))$

Vale anche per $\Theta,\Omega$ 

### Simetrica

$g(n) = \Theta(f (n)) \iff f (n) = \Theta(g(n))$

### Simmetrica trasposta


$g(n) = O(f (n)) \implies f (n) = o(g(n))$  
$g(n) = \Omega(f (n)) \implies f (n) = \omega(g(n))$  


## Costo e Complessità computazionale

> **costo computazionale** è il costo dell' algoritmo 
> **complessità computazionale** è il costo per risolvere un problema


## Caso Medio, Pessimo, Ottimo

> **Caso ottimo:** descrive il comportamento in condizioni ottimali
> **Caso pessimo:** descrive il comportamento in condizioni sfavorevoli
> **Caso medio:** descrive il comportamento medio su tutti i possibili input

## Analisi Ammortizzata


> L’analisi ammortizzata è un metodo per valutare il costo medio di una
sequenza di operazioni

<details>
<summary>
costo medio vs costo ammortizzato
</summary>

- costo medio: media del costo di una singola operazione
- costo ammortizzato: media del costo di una sequenza di operazioni

</details>


### Metodo dell'Aggregazione

> determiniamo un limite superiore al costo totale di una sequenza di n operazioni e dividiamo per n



### Metodo con Accantonamenti

- Assegniamo un costo ammortizzato ad ogni operazione
- Ogni operazione viene addebitata con il suo costo ammortizzato
- Dopo ogni operazione, salviamo come credito la differenza tra il
- suo costo ammortizzato e costo reale
- Accumuliamo il credito collezionato durante l’esecuzione
- Se il costo reale è piu alto del costo ammortizzato, usiamo il credito `
- Il costo ammortizzato è corretto se il credito non è mai negativo



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