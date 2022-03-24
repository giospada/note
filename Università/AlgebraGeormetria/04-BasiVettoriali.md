# Basi vettoriali

 **def**: sia V uno spazio vettoriale, una base di vettoriale $\{v_1,\dots,v_n\}$ tali che:
 1. $v_1,\dots,v_n$ generano V  cioè V è l'insieme lineare generato da $v_1,\dots,v_n$ ($V=<v_1,\dots,v_n>$)
 2. $v_1,\dots,v_n$ sono linearmente indiependenti
 
<details>
<summary>
esempio in $\mathbb{R}^2$
</summary>

$v_1=(1,0)$,$v_2=(0,1)$
sono lineramente indiependenti perche sono multiplo dell'altro e generano $\mathbb{R}^2$

</details>


Uno spazio vettoriale V si dice **finitamente generato** se $V= <v_1,\dots,v_n>$( $\mathbb{R}[x]$ non è finitamente generato)



**Prop** sia $V=<v_1,\dots,v_n>$ spazio vettorialiale ginitamenteo generato allora esiste un sottinsieme di $\{v_1,\dots,v_n\}$ he è una base di V

<details>
<summary>
dimostrazione
</summary>

Se $v_1,\dots,v_n$ sono indipendenti $\{v_1,\dots,v_n\}$ sono una base se sono dipendenti per la prop  uno di essi è combinazione lineare degli altre sia $v_k$)

Prop 3.1.8 : $<v_1,\dots_,v_{k-1},v_{k+1},\dots,v_n>=<v_1,\dots,v_k,\dots,k_n>$

cancelliamo tutti i vettori finche non abbiamo tutti i vettori indipendenti

</details>



**Teorema:4.1.4** Siano $v_1,\dots,v_n \in V$:
1.$\{v_1,\dots,v_n \}$ è una base  $\iff$ è un insieme minimale di generatori
2.$\{v_1,\dots,v_n \}$ è una base  $\iff$ è un insieme massimale di vettori lineramente indipendenti 


<details>
<summary>
massimale e minimale def
</summary>

Un insieme di vettori con una certa proprità si dice minimale se ogni suo sottoinsieme proprio non ha più quella proprietù e massimale se ogni suo sovrainsieme proprio non ha più la proprietà

</details>


## Teorema del Completamenteo


Sia V uno spazio vettoriale con base $\{v_1,\dots,v_n\}$ e siano $\{w_1,\dots,w_m\}$  linearmente indipendenti con $m\leq n$ 
possiamo aggiungere a $\{w_1,\dots,w_1\}, n-m$  vetotri di $\beta$ per ottenere una base 


**Prop: 4.2.2** tutte le basi di uno spazio vettoriale (finitamente generato), hanno lo stesso numero di elementi


**Prop: 4.2.4** Sia uno spazio vettoriale V e W un suo sottospazio $dim(V)>dim(W)$ e se $dim(V)=dim(W)$ allora $V=W$


**Prop: 4.2.6** Sia V uno spazio vettoriale di dimensione  n e ${v_1,\dots,v_n}$  dei vettori appartenenti a V, allora le seguenti affermazioni sono equivalenti:
a. ${v_1,\dots,v_n}$ sono una base di V
b. $v_1,\dots,v_n$ sono linearmente indipendenti
c. $<v_1,\dots,v_n>$ generano V

**Prop: 4.2.8**  Sia B una base ordinata dello spazio vettoriale V allora esiste una sola combinazione lineare della base (un nupla di scalari) che genera il vettore $v\in V$


### Basi canoniche

- $\mathbb{R}^n$ ha dimensione **n** es.$<(1,\dots,0),(0,1\dots,0),\dots,(0,dots,1)>$
- $\mathbb{R}^n[x]$ ha dimensione **n+1** es.$<(x^n,\dots,0)(0,x^{n-1},\dots,0)\dots,(0,\dots,1))>$
- $\mathbb{M}_{M,N}(R)$ ha dimensione **N x M** es (troppo lungo da scrivere)




## Uso dell'algoritmo di gauss sugli spazi vettoriali

**Prop 4.3.1**: data una matrice $A \in M_{n,m} (\mathbb{R})$ le operazioni elementerai di riga non cambiano lo sottospazio $\mathbb{R}^n$ generato dai vettori riga $A$


**Prop 4.3.3** Se una matrice A è a scala per riga, i suoi vettori riga non nulli sono linearmente indipendenti

### Utilizzo negli esercizi

**trovare una base di un sottospazio** (cercare se una serie di vettori sono linearmenete indipendenti):
- creare la matrice che contiene come righe i vettori
- utilizzare l'algorimto di gaus per creare una matrice a scala
- i vettori formati da righe non nulle sono linearmente indipendenti


**per ottenere una base di un sottospazio $\mathbb{R}^n$**
- creare una matrice a scala con i vettori presi in considerazione
- i vettori $v_1,\dots,v_m$ devono avere $m<n$, aggiungiamo $n-m$ righe e le completiamo con dei vettori linearmente indipendenti	 
