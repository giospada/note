
# Calcolo Combinatorio


> permutazioni: contano l'ordine degli elementi

> combinazioni: contano il numero di set diversi

## Fattorial (permutazioni)


$n!= 1*2*3*4*5*...*(n-1)*n, n\in \mathbb{N}$ , $0!=1$

il **fattoriale** si usa per **contare le permutazioni di una lista di elementi diversi**.

## Coefficente Binomiale (combinazioni)


$n \in \mathbb{N}, m \in \mathbb{N}$


$\frac{n!}{k!(n - m)!} = \binom{n}{m} = {}^{n}C_{m} = C_{n}^m$

il **binomiale** si usa per contare **quanti sottoinsiemi partendo di m elementi posso formare partendo da un insieme di n**(non contano gli ordini,combinazioni).

**Proprietà**:

1.  $\binom{n}{k}=\binom{n}{n-k}$
2.  $\binom{n+1}{k}=\binom{n}{k-1}+\binom{n}{k}$

<details>
    <summary>
    Prova coefficiente binomiale
    </summary>

1. dimostrazione della prima prioperietà:  
se ci si pensa noi stiamo selezionando combinazioni k elementi partendo da un insieme di n, facendo così creaiamo un altro inieme di n-k elementi complementare per cui ha le stesse combinazioni
2. dimostrazione seconda proprietà:

![](../img/dimbinomialep1.png)
![](../img/dimbinomialep2.png)
</details>


## Il binomio di Newton

Come si calcola il binomio $(a+b)^n=?$

TODO: spiegare con parole tue come si calcola il coefficente di ogni binomio

**Formula del binomio di newton**

$(a+b)^n=\displaystyle \sum^{n}_{k=0} \binom{n}{k} a^{n-k}*b^k$
