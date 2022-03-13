# Combinazioni lineari e indipendenza lineare


## Combinazione lineare

**Combinazione lineare:** dato uno SV $V$ i cui vettori sono $v_1,...\ v_n$ e dati $\lambda_1,...\ \lambda_n \in \mathbb{R}$, il vettore $w = \lambda_1v_1+...+\lambda_n v_n$ si dice *combinazione lineare* di $v_1,...\ v_n$ con scalari $\lambda_1,...\ \lambda_n$.

**Sottospazio generato:** dato uno SV $V$ e un insieme di vettori $\{v_1,...\ v_n\}$ di $V$, il *sottospazio generato* dai vettori $v_1,...\ v_n$ è l'insieme di tutte le loro combinazioni lineari, che tradotto in simboli è: $\langle v_1,...\ v_n \rangle = \{ \lambda_1v_1 + ... + \lambda_nv_n\ |\ \lambda_1, ...\ \lambda_n \in \mathbb{R} \}$

Osservazioni:

- il sottospazio generato da un singolo vettore dello SV $v \in V$ è l'insieme dei multipli di $v$, ovvero $\langle v  \rangle = \{ \lambda v\ |\ \lambda \in \mathbb{R} \}$
- il sottospazio generato dal vettore nullo invece è il sottospazio banale contenente solo il vettore nullo, ovvero $\langle 0 \rangle = \{ 0 \}$

Generatori: dato uno SV $V$ e un insieme di vettori di $V\ \{v_1, ...\ v_n \}$, si dice che $v_1,...\ v_n$ *generano $V$* o che  $\{v_1, ...\ v_n \}$ è un *insieme di generatori* di $V$ se $V = \langle v_1, ...\ v_n\rangle$.

PROP: siano $V$ uno SV e  $\{v_1, ...\ v_n \}$ un insieme di vettori di $V$, si ha che $\langle v_1, ...\ v_n\rangle$ è un sottospazio vettoriale di $V$.

Inoltre se $Z$  è un sottospazio vettoriale di $V$  contenente $v_1,...\ v_n$, allora $\langle v_1, ...\ v_n\rangle  \subseteq Z$, cioè $\langle v_1, ...\ v_n\rangle$ è *il più piccolo* sottospazio vettoriale di $V$ contenente $v_1, ...\ v_n$.



## Combinazione Lineare

Sia $V$ uno spazio vettoriale $v_1,\dots,v_n \in V$. Un vettore $v$ si dice combinazione lim di $v_1,\dots,v_n$ se esistono $d_1,\dots,d_n\in\mathbb{R}$ tali che $v=d_1v_1+\dots+v_nd_n$


**Def** sia $V$ uno spazio vettoriale $v_1,\dots,v_n \in V$ $<v_1,\dots,v_n \in V>:=\{d_1v_1+\dots+d_nv_n|d_1,\dots,d_n \in \mathbb{R}\}$

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


## Linearmente indimpendenti

**Def**: V spazio vettoriale $v_1,\dots,v_n\in V$ si dicono linearmente indipendenti se l'unica loro combinazione lineare che da $\underline{0}$ ()è quella con i coeffincenti tutti nulli)

## Linearmente dipendenti

$v_1,\dots,v_n$ si dicono dipendenti se non sono linearmente indipendenti, cioà $\exists d_1,\dots,d_n \in \mathbb{R}$  dove non sono tutti nulli tale che $d_1v_1+\dots+d_nv_n=\underline{0}$

**Oss**: se un insieme di vettori contiene $\underline{0}$ allora i vettori  sono (sempre) dipendenti


**prop(3.24)** sia V uno spazio vettoriale $v_1,\dots,v_n$ sono dipendenti $\iff$ almeno uno di essi è combinazione lineare degli altri

<details>
<summary>
dimostrazione
</summary>

Ip: $v_1,\dots,v_n$ dipendenti esistono $d_1,\dots,d_n$ non tutti nulli, quindi $\exists d_k\neq 0$

$\iff$ prima parte:
$d_kv_k=d_1v_1-\dots-d_{k-1}v_{k-1}-d_{k+1}v_{k+1}-\dots-d_nv_n$

quindi
$v_k=\frac{(d_1v_1-\dots-d_{k-1}v_{k-1}-d_{k+1}v_{k+1}-\dots-d_nv_n)}{d_k}$

quindi $v_k$ è combinazione lineare degli altri

$\iff$ prima seconda parte:
$v_k=d_1v_1+\dots+d_{k-1}v_{k-1}+d_{k+1}v_{k+1}+\dots+d_nv_n$
$d_1v_1+\dots+d_{k-1}v_{k-1}+v_k+d_{k+1}v_{k+1}+\dots+d_nv_n$


</details>

 **def**: sia V uno spazio vettoriale, una base di vettoriale $\{v_1,\dots,v_n\}$ tali che:
 1. $v_1,\dots,v_n$ generano V  cioè V è l'insieme lineare generato da $v_1,\dots,v_n$ ($V=<v_1,\dots,v_n>$)
 1. $v_1,\dots,v_n$ sono linearmente indiependenti
 
<details>
<summary>
esempio in $\mathbb{R}^2$
</summary>

$v_1=(1,0)$,$v_2=(0,1)$
sono lineramente indiependenti perche sono multiplo dell'altro e generano $\mathbb{R}^2$

</details>


Uno spazio vettoriale V si dice finitamente generato se $V= <v_1,\dots,v_n>$

<details>
<summary>
esempio
</summary>

$\mathbb{R}[x]$ non è finitamente generato

</details>


**Prop** sia $V=<v_1,\dots,v_n>$ spazio vettorialiale ginitamenteo generato allora esiste un sottinsieme di $\{v_1,\dots,v_n\}$ he è una base di V

<details>
<summary>
dimostrazione
</summary>

Se $v_1,\dots,v_n$ sono indipendenti $\{v_1,\dots,v_n\}$ sono una base se sono dipendenti per la prop  uno di essi è combinazione lineare degli altre sia $v_k$)

Prop 3.1.8 : $<v_1,\dots_,v_{k-1},v_{k+1},\dots,v_n>=<v_1,\dots,v_k,\dots,k_n>$

cancelliamo tutti i vettori finche non abbiamo tutti i vettori indipendenti

</details>


Un insieme di vettori con una certa proprità si dice minimale se ogni suo sottoinsieme proprio non ha più quella proprietù e massimale se ogni suo sovrainsieme proprio non ha più la proprietà


**Teorema:4.1.4** Siano $v_1,\dots,v_n \in V$:
1.$\{v_1,\dots,v_n \}$ è una base  $\iff$ è un insieme minimale di generatori
2.$\{v_1,\dots,v_n \}$ è una base  $\iff$ è un insieme massimale di vettori lineramente indipendenti 


Dimostrazione sul libro


## Teorema del Completamenteo


Sia V uno spazio vettoriale con base $\{v_1,\dots,v_n\}$ e siano $\{w_1,\dots,w_m\}$  linearmente indipendenti allora $m\leq n$

Inoltre possiamo aggiungere a $\{w_1,\dots,w_1\}, n-m$  vetotri di $\beta$ per ottenere una base 


**Prop: 4.2.2** tutte le basi di uno spazio vettoriale (finitamente generato), hanno lo stesso numero di elementi


## Basi canoniche

in $\mathbb{R}^n, \beta=\{e_1,\dots,e_n\},$ $e_1=(1,\dots,0), e_2=(0,1,\dots,0), e_n=(0,\dots,1)$ 
$v=(a_1,\dots,a_n)\in \mathbb{R}^n$  $v=a_1(1,\dots,0)+a_2(0,1,\dots,0)+\dots+e_n=(0,\dots,1)$
$\implies <e_1,\dots,e_n> = \mathbb{R}^n$ sono indipendenti $\mathbb{R}^n$ base di dimensione n

Base di $\mathbb{R}_n[x]=\{a_nx^n+\dots+a_1x+a_0|a_0,\dots,a_n \in \mathbb{R}\}$ quindi $\mathbb{R}_n[x]$ ha dimensione $n+1$

$M_{m,n}$ ha dimensione $n\times m$




### Uso dell'algoritmo di gauss sugli spazi vettoriali

1. L'algoritmo di Gauss non cambia il sottospazio generato dalle righe di una matrice
2. le righe non nulle di una matrice a scala sono indip



data una matrix$\begin{pmatrix}R1\\R2\\\vdots\\R_k\end{pmatrix}$Gauss $\to$ $\begin{pmatrix}\bar{R1}\\\bar{R2}\\\vdots\\\bar{R_k}\end{pmatrix}$

$<R_1,\dots,R_k>=<\bar{R_1},\dots,\bar{R_k}>$




