
# Funzioni

$f: A \rightarrow B$ $x \overrightarrow{f} f(x)$:
- A è il dominio di $f$ 
- B è il codominio di $f$
- $f$ è la legge di associazione

> f è la legge d'associazione che associa un elemento nell'insieme A in un insieme B (la funzione è definita dal: dominio,codominio e legge di associazione ($A,B,f$))  
$\forall x \in A, \exists! b \in B : f(x) = b$ 


due funzioni sono uguali se e solo se il dominio il codominio e la legge di associazione sono uguali:
<details>

$f: A \rightarrow B \\ f': A'\rightarrow B' \\ \begin{cases} A=A' \\ B=B' \\ f=f'\end{cases}$
</details>



### Iniettività

> prioprietà iniettiva (1-1): tutti gli elementi del codominio sono associati a un elemento del codominio diverso
 $f: A \rightarrow B$ se $\forall a \in A,\forall a' \in A : a\neq a' \rightarrow f(a) \neq f(a')$

> l'inniettività dipenda dal dominio

<details>
    <summary>
    esempio
    </summary>

$f(n)=n^2$ non è (1-1) perchè $f(-1)=1=f(1)$  
ma la si può far diventare mettendo come dominio R+

$f(n)=n^3$ è (1-1)
</details>

### Surettività

> surrettiva (su) ogni elemento del codominio deve avere un elemento del dominio per cui f(a)=b
$\forall b \in B, \exists a \in A : f(a)=b$

> la surrettività dipenda dal codominio

<details>
    <summary>
    esempio
    </summary>

$f: A \rightarrow B$  
$f(n)=n^2$ non è (su) perché $\forall b \in B, \nexists a \in A : f(a)=b$  
ma la si può far diventare mettendo come codominio R+

$f(n)=n^3$ è (su)
</details>

### Biunivoca

> Una funzione sia surrettiva che invettiva è detta biunivoca e quindi è invertibile

$f: A \rightarrow B$ è invertibile
$f^{-1}: A \rightarrow B$ e vuol dire che:
- $\forall a \in A: f^{-1}(f(a))=a$  
- $\forall b \in B: f(f^{-1}(b))=b$  

$f$ è ivertibile $\leftrightarrow f$ è biunivoca 

### Inisme immagine
> l'immagine di una funzione sono tutti gli elementi di b che sono associati con a

$\text{Img} f = \{ b \in B | \exists a \in A : f(a)=b \}$  
$\text{Img} f \subseteq B$

## Cardinalità

perchè vengono estesi i numeri razionali a quelli reali

> la cardinalità di un insieme è il numero di elementi di un insieme

due insiemi sono **equipotenti** solo se i due insiemi **hanno la stessa cardinaltà**.  
Si può dimostrare  due insiemi sono equipotenti se c'è una **corrispondenza biunivoca** (molto utile con gli insiemi infiniti).

$N$ e $Z$ sono inifiniti
$N \subsetneqq Z$

$N$ e $Z$ sono equipotenti


<details>
    <summary>
    dimostrazione che  N e Z sono equipotenti
    </summary>

per dimostrare che $\mathbb{N}$ e $\mathbb{Z}$ sono equipotenti creaiamo una funzione biunivoca tra i due 

$f(n)= \begin{cases} n/2 & \text{se n è pari} \\ -\frac{n+1}{2} & \text{se n è pari} \end{cases}$

</details>


## Numberailità

> un insieme è numberabile se esiste una funzione $f : N \rightarrow A$ è biunivoca 

> lemma: è un piccolo teorema

> (Lemma) A è numerabile se è solo se 
$f_1 : A \rightarrow \mathbb{N}$ è surrettiva  
$f_2 : \mathbb{N} \rightarrow A$ è surrettiva


si può provare che l'insieme dei numeri razionali è numerabile

<details>
    <summary>
    prova numerabilità di Q    
    </summary>

come prima cosa si crea una tabella che contiene tutti i numeri razionali, a quel punto si collega ogni numero naturale a un numero razionale

![](../img/qnumerabile.png)

</details>


## Funzioni Crescenti e Decrescenti

$I \subset \mathbb{R}$

1. f si dice **crescente** se $\forall x, y \in I : x < y \implies f(n) \le f(y)$
2. f si dice **decrescente** se $\forall x, y \in I : x < y \implies f(n) \ge f(y)$


## Funzioni Pari e Dispari

data una funzione 
$f: A \rightarrow \mathbb{R}$

$f(x)=f(-x) \forall x \in A$ la funzione è pari    
$-f(x)=f(-x) \forall x \in A$  la funzione si dice dispari

<details>
    <summary>
    esempio 
    </summary>

$y=x^2$ è una funzione pari

TODO: aggiungere il grafico

$y=x^3$ è una funzione dispari

TODO: aggiungerei l fico
</details>



