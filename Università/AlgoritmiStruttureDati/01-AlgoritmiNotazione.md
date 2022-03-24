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

$o(g(n)) = \{f(n) :$ per qualsiasi costante c > 0, esiste una costante $n_0 > 0$ tale che  $0 ≤ f(n) < cg(n) \forall n ≥ n_0\}$

oppure
$\displaystyle \lim_{x \rightarrow +\infty} \frac{f(x)}{g(x)}=0$


###  omega piccola

Limite asintotico maggiore stretto, indica una funzione che ha una crescita maggiore

$\omega(g(n)) = \{f(n) :$ per qualsiasi costante c > 0, esiste una costante $n_0 > 0$ tale che    $cg(n) <  f(n), \forall n ≥ n0\}$


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
- Se il costo reale è piu alto del costo ammortizzato, usiamo il credito
- Il costo ammortizzato è corretto se il credito non è mai negativo


