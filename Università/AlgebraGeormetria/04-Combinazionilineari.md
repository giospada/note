# Basi vettoriali

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

