# Integrale


L'integrale di una funzione calcola l'area che c'è tra essa e l'asse delle x in un determinato intervallo.


## Somme di Reimann
1. come prima cosa divido l'intervallo in n parti, l'intervallo va da $[a,b]$, fisso un $n \in \mathbb{N}$ qundi ogni pezzo è di lunghezza $h=\frac{b-a}{n}$ quindi avremo $a=x_0,x_1=x_0+h,x_k=x_0+n\times h=b$

2. $\forall k=0,1,...,n-1$ scelgo un punto (arbitrario) $\xi_{k+1} \in [x_k,xk+1], \text{se } k=0 ,\space \xi \in [x_0,x_1]$ 
3. somma n-esima $S_n=\sum^n_{k=1} f(\xi_k)*h$



> come la continuità è relazionata con l'integrale

**Teorema**: sia **f** continua su **[a,b]** sia $(S_n) n \in \mathbb{N}$ una famiglia di somme di riemenn. allora $\exists \displaystyle \lim_{n \rightarrow +\infty}  S_n$ finito e indipendente dalle scelte degli $\xi$ ( xi è la variabile che si mette nella funzione per calcolarne l'altezza in quel punto), Notazione $\displaystyle \lim_{n \rightarrow \infty} S_n= \int_{a}^b f(x) dx$


### Osservazioni 


**osservazione-1** se $a=b \text{ allora }  S_n=0 \space \forall n \in \mathbb{N} \int^b_a f(x) dx=0$

**osservazione-2** se $f(x)=c ,\space \forall x \in [a,b], S_n=c(b-a), \space \int_a^b c \space dc=c(b-a)$

**osservazione-3** se $S_n=\sum_{k=1}^n f(\xi_k)\times h \space \text{ dove h è uguale}=\frac{b-a}{n}$
 le somme di reimann si possono definire qualsiasi $f$ continua
 
**osservazione**: esistono funzioni discontinue per le quali il $\displaystyle \lim_{n \rightarrow \infty} S_n$ dipende dalla scelta di $\xi_k$ oppure non esiste

**osservazione** se $f$ ha un numero finito di discontinuità con salto finito (senza limiti che vanno a $\pm \infty$),  $\int_a^b f$ + definito

### Proprità

#### Linearità
 $f,g$ continua su $[a,b], \lambda \varphi \in \mathbb{R}$ allora $h\times[a,b]\to \mathbb{R}, h(x)=\lambda f(x)+ \varphi g(x)$ h è integrabilie $\int_a^b [\lambda f(x)+\varphi g(x)] dx = \lambda \int^a_b f + \varphi \int^b_a g$  (**limite della somma è uguale alla somma dei limiti**)

#### Additionalità

> la somma di due integrali della stessa funzione con punto il limite opposto in comune allora è equivalente alla l'integrale degli altri due estremi

sia $f [a,b] \to \mathbb{R}$ continua , $c \in [a,b] \text{ allora } \int_a^b f= \int_a^c f + \int^b_c f$ 


<details>
<summary>
Convenzione
</summary>

> semplicemente l'integrale delle parti dei punti invertiti è uguale all'integrale negato questo per come si calcola l'integrale

**convenzione**  $f :\mathbb{R} \to \mathbb{R}, a,b \in \mathbb{R} : a> b, \int_a^b f(x) dx = - \int^a_b f(x) dx$

Con la convenzione se $f:\mathbb{R} \to \mathbb{R}$ è continua $\forall a,b,c \in \mathbb{R}$ vale $\int^b_a f = \int^c_a f+ \int_c^b f$ anche se $a<b<c \text{ si inverte l'ultimo integrale}$

</details>

#### Monotonia

> se una funzione è sempre maggiore uguale in un intervallo chiuso allora sara maggiore uguale anche l'integrale

**Monotonia** $f,g [a,b] \to \mathbb{R}$ continue, $f(x)\le g(x) \forall x \in [a,b]$ se $a<b$ allora $\int^b_a f(x) dx \le \int^b_a g(x) dx$





## Teorema della media
**Teorema** $S_b = \sum^n_{k=1} f(\xi_k) \frac{b-a}{n}$ $\frac{S_n}{b-a}= \frac{ \sum^n_{k=1} f(\xi_k)}{n}$ 

**Teorema**: della media integrale,  $f:[a,b]\to \mathbb{R}$ continua $\exists c  \in [a,b] : \frac{1}{b-a}\times \int_a^b f(x) dx=f(c)$

### Dimostrazione

<details>
<summary>
teorema dei valori intermedi 
</summary>

**teorema (valori intermedi)**: $f:[a,b] \to \mathbb{R}$ continua siano $x_0,x_1 \in [a,b] : f(x_0) < f(x_1) \text{ allora } \forall y  \in [f(x_0),f(x_1)]  \text{ allora } \exists c \in [a,b] \text{tale che } f(x) = c$

</details>


**Dim** Uso del toerema dei valori intermedi  $\exists x_0 ,x_1 \in [a,b] f(x_0) \le f(x \le f(x_1) \text{ dove x_0 è il minimo e x_1 è il massimo } \forall x \in [a,b]$ proprietà di monotonia  $\int^b_a f(x_0) dx \le \int_a^b f(x) dx \le \int_a^b f(x_1) dx$  essendo che x_0 è una  constante  per il teorema precedente $f(x_0)(b-a)  \le \int_a^b f(x) dx  \le f(x_1) (b-a) \to  f(x_0) \le \frac{1}{b-a} \int_a^b f(x)  dx \le f(x_1)$ quindi abbiamo $y \in [f(x_0),f(x_1)] \to \exists c \in [a,b] \text{tale che } f(c)=\frac{1}{b-a} \int^b_a f(x) dx$      
