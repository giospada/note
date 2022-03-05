# Spazi Vettoriali

## Piano cartesiano

Piano cartesiano a due dimensioni $\mathbb{R}^2=\{(x,y)|x,y\in \mathbb{R}\}$ 

$\mathbb{R}^2$ è in corrispondentza biunivoca con i vettori del piano applicati all'origine

 $\mathbb{R}^2$ è in corrispondentza biunivoca anche con in punti del piano


## Addizione
In $\mathbb{R}^2$ supponiamo somme di 2 elementi $v_1=(5,7),v_2=(-1,4) \in \mathbb{R}^2, v_1+v_2=(5+(-1),7+4)=(4,11)$

e vale anche in un piano con n dimensioni $\mathbb{R}^n=\{(x_1,x_2,\dots,x_n)|x_1,x_2,\dots,x_n\in \mathbb{R}\}$  



### Proprità Addizzione

- associativa
- commutativa
- ammette un'elemento neutro $(0,0)$ indicato come $\underline{0}$
- ogni elemento ha un opposto ( che sommato con il vettore da l'elemento neutro)

## Moltiplicazione
Supponiamo di moltiplicare un elemento per un numero 2 reale $v_1(x,y), d\in \mathbb{R}, dv=(dx,dy)$

e vale anche in un piano con n dimensioni $\mathbb{R}^n=\{(x_1,x_2,\dots,x_n)|x_1,x_2,\dots,x_n\in \mathbb{R}\}$  

### Proprità moltiplicazione

- ammette l'elemento neutro 1
- associatività tra due numeri e un vettore,  $(\lambda\mu) u =\lambda(\mu u)\quad \forall  u \in V\ \&\ \forall \lambda,\mu \in \mathbb{R}$
- distributiva tra un numero e due vettori $\lambda({u+v})=\lambda u+\lambda v\quad \forall  {u,v} \in V\ \&\ \forall \lambda \in \mathbb{R}$
- distributiva tra due numero e un vettori $(\lambda+\mu){u}=\lambda u+\mu u\quad \forall  {u} \in V\ \&\ \forall \lambda,\mu \in \mathbb{R}$

## Polinomi

Polinomi a coefficenti in $\mathbb{R}, \mathbb{R}[x]=\{a_0+a_1+x+\dots+a_nx^n|m\in \mathbb{R},a,\dots,a_n\in \mathbb{R}\}$

rappresenta anch'esso uno spazio vettoriale


## Sottospazio

Sia W un sottoinsieme dello spazio vettoriale V. Diremo che W è un sottospazio vettoriale di V se soddisfa le seguenti proprietà

- (1) $W \ne \emptyset$
- (2) W è chiuso rispetto alla somma, cioè $\forall{ u,v} \in W$ si ha che ${u+v}\in W$
- (3) W è chiuso rispetto al prodotto per scalari, cioè $\forall u \in W$ e $\forall \lambda \in \mathbb{R}$  si ha che $\lambda u\in W$


allora **valgono anche le seguenti proprità**:
- (1') $\underline{0}\in W$
- (23) $\forall d,\mu\in \mathbb{R}, \forall u_1,u_2 \in U, ( d u_1+\mu u_2 )\in W$


> Nota
> valgono le proprità $1,2,3$ se e solo se ($\iff$)$1',2,3$ 
> valgono le proprità $2,3$ se e solo se vale  ($\iff$)$23$ 


osserviamo che poiché W non è vuoto, e $\lambda  u \in W\quad \forall \lambda \in \mathbb{R}$, allora prendendo un vettore qualsiasi di W e moltiplicandolo per $\lambda = 0$ si ottiene che $0_v \in W$. questo ci permette di sostituire la prima proprietà con


il sottospazio vettoriale W di V è quindi uno spazio vettoriale con le operazioni di V ristrette a W.

la seconda proprietà infatti assicura la restrizione della somma

$$
+v|w\times w : W\times W \to W
$$

analogalmente la proprietà 3 assicura la restizione a $\mathbb{R} \times W$ del prodotto per scalari definito su $\mathbb{R}\times W$ dia come risultato un vettore di W.

<details>
<summary>
esempio
</summary>

sia $U = \{  (x,y) \in \mathbb{R}^2 | y=mx \}$,  è un sottospazio di $\mathbb{R}^2$

sia $U = \{  (x,y) \in \mathbb{R}^2 | y=5x+4 \}$, non è un sottospazio di $\mathbb{R}^2$ perchè non ha l'elemento nullo

</details>

## Sottospazio banale 

Se V è sottospazio di $U=\{\underline{0}\}$ è sottospazio e si dice sottospazio banale o sosttospazoi nullo

### Sottospazi di R


In Generale se prendiamo due punti che non appartengono alla stessa retta per l'origine, il più piccolo sottospazio che li contiene entrambi è il piano

 Abbiamo scoperto che gli unici sottospazi di $\mathbb{R}^2$ sono:
 1. $\{(0,0)\}$
 2. le rette per l'origine
 3. $\mathbb{R}^2$
 



## Combinazione Lineare

Sia $V$ uno spazio vettoriale $v_1,\dots,v_n \in V$. Un vettore $v$ si dice combinazione lim di $v_1,\dots,v_n$ se esistono $d_1,\dots,d_n\in\mathbb{R}$ tali che $v=d_1v_1+\dots+v_nd_n$


Def sia $V$ uno spazio vettoriale $v_1,\dots,v_n \in V$ $<v_1,\dots,v_n \in V>:=\{d_1v_1+\dots+d_nv_n|d_1,\dots,d_n \in \mathbb{R}\}$

Propo (3.1.5) Sia $V$ spazio vettoriale $v_1,\dots,v_n\in V$ , allora $<v_1,\dots,v_n> \subseteq Z$

### Dimostrazione

$\underline{0}=0v_1+\dots+v_n \in <v_1,\dots,v_n>$

Siano $u_1,u_2 \in <v_1,\dots,v_n>$   
$u_1 = d_1v_1+\dots+d_nv_n$
$u_2 = \beta_1+\dots+\beta_nv_n$
$u_2+u_1 = \beta_1+\dots+\beta_nv_n + d_1v_1+\dots+d_nv_n = (d_1+\beta_1)v_1+\dots+(d_n+\beta_n)v_n \in <v_1,\dots, v_n>$

$u_2+u_1 = \beta_1+\dots+\beta_nv_n + d_1v_1+\dots+d_nv_n = (d_1+\beta_1)v_1+\dots+(d_n+\beta_n)v_n \in <v_1,\dots, v_n>$




mostriamo che $<v_1,\dots,v_n> \subseteq Z$ Sia $v \in <v_1, \dots>$


### Nel piano Cartesiano


in $\mathbb{R}^2$  $<v>$ è una retta per $(0,0)$  

In $\mathbb{R}^3<v,w>$ è una retta appartiene $(0,0,0)$  



Sia $V$ spazio vetoriale $v_1,\dots,v_n \in V$ e $w= d_1v_1+\dots+d_nv_n$ allora $<v_1,\dots,v_n>=<v_1,\dots,v_n,w>$













