# Funzioni in R^n



## Succcessioni in $\mathbb{R}^n$

Una successione in $\mathbb{R}^n$ è una famiglia di $(x_k) k \in \mathbb{N}$ dove $x_k \in \mathbb{R}^n$ $\forall x \in \mathbb{N}5$ $x=(x_k^1,x_k^2,\dots,x_k^n) \in \mathbb{R}^n$ $\forall x \in \mathbb{N}$ (nota non è un elevamento a potenza è un indice che va da 1 a n)


### Successione convergente
**Def** successione convergente $(x_k) k \in \mathbb{N}$ successioni in $\mathbb{R}^n, x \in \mathbb{R}^n$ .$\displaystyle \lim_{k \rightarrow \infty}x_k=x$ Si dice $\displaystyle \lim_{k \rightarrow +\infty} x^1_k = x^1 , \dots, \displaystyle \lim_{k \rightarrow +\infty} x^n_k = x^n$


**oss**: $(x_k)_{k \in \mathbb{N}},$ in $\mathbb{R}^n$ $x_k \to x \in \mathbb{R}^n \iff |x_k -x |\to 0$(con k che tende a +infinito)

## Funzioni di più variabili 
 
**Def**(grafico):Siano $A \subseteq \mathbb{R}^n, B \subseteq \mathbb{R}^q$ dove $\space n,q \in \mathbb{N}$ , Data$f:A\to B$ il grafico è $Graf(f)=\{(x,f(x))\} \subseteq A \times B$



**Funzioni Scalari**:
- $q=1, A\subset \mathbb{R}^n , f:A \to \mathbb{R}$
- $n=1, q>1 I \subseteq \mathbb{R}, f:I \to \mathbb{R}^q$

### Funzione Continua

**Def**(funzione continua): Dati $A \subseteq \mathbb{R}^n, B\subset \mathbb{R}^q$. Sia $f: A \to B$ con $\bar{x} \in A$ si dice f continua in $\bar{x}$ se vale$\forall (x_k)_{k \in \mathbb{N}}$,( dove $(x_k)$ sono successioni in $A$), $\displaystyle \lim_{k \rightarrow \infty} (x_k)=\bar{x}$ $\implies \displaystyle \lim_{k \rightarrow \infty} f(x_k)=f(\bar{x})$   (convergenza in $\mathbb{R}^q$) 

> Nota
>Si dimostra che tutte le funzioni "elementari" sono continue 



### Dimostrare la continuità di una successione

**oss** $f:A\to B$ è continua in $\bar{x}$ $\iff \forall \varepsilon  >0 \exists \delta_{\varepsilon}$ tale che $|f(y)-f(\bar{x})| < \varepsilon$ $\forall x \in A$ con $|y-\bar{x}|<\delta$



Si dimostra che se  $f_1,f_2,\dots,f_p:\mathbb{R}^n\to \mathbb{R}$ scalari sono continue, allora ogni insieme $A=\{x\in\mathbb{R}|f(x)_1<c_1,\dots,f(x)_p<c_p\}$



### Funzione radicale

$f: \mathbb{R}^2 \to  \mathbb{R}$ tale che $\exists g:[0; +\infty[ \to \mathbb{R}$ per cui $f(x,y)=g(|(x,y)|)=g(\sqrt{x^2+y^2})$



### Insiemi di livello

gli insiemi di livello sono un modo di rappresentare le funzioni che consiste nel studiare una funzione ad  un livello minore, per esempio studiare una funzione in $\mathbb{R}^3$ come diverse funzioni in $\mathbb{R}^2$


<details>
<summary>
es
</summary>


$f:\mathbb{R}^2 \to \mathbb{R}$
$A \subseteq \mathbb{R}^2, f:A \to \mathbb{R}, b \in \mathbb{R}$ l'insieme di livello b di f è $L_b=\{(x,y)\in A | f(x,y)=b\}=f(b)$

</details>



### Piani

**Def**(piano): un piano è una funzione $f: \mathbb{R}^2 \to \mathbb{R},\space$, con la seguente focmula  $f(x,y)= ax+by+c \space$ dove $(a,b,c)\in \mathbb{R}^3$ (il $Graf(f)$ è un piano )