# Applicazini lineari e nuclei

## Funzioni

**def**: $f:A \to B$ una legge che per ogni elemento di A associa un solo elemento di B è un sottoinsieme $\Gamma$ di $A\times B$ tale che $\forall a \in A$ , $\exists ! b$ tale che $(a,b) \in \Gamma$, f è su $x \forall b \in B \exists a \in A$ tale che $f(a)=b$

### Immagine

$Im\space f=\{f(a)|a\in A\}={b\in B | \exists a \in A, b=f(a)}$

### Iniettiva
f è iniettiva se $a_1 \neq a_2 \implies f(a_1)\neq f(a_2)=$, oppure  $f(a_1)= f(a_2) \implies a_1 = a_2$

### Composta

Se  $f: A \to B$, $g:B \to C$ allora $g \cdot f: A \to C$ 


## Applicazioni lineari 

V,W spaziz vettoriali, $F: V \to W$ si dice applicazione lineare di  se :
- $F(v+u)=F(u)+F(u), \forall v,u \in V$ 
- $\lambda F(v)=F(\lambda u)\forall v \in V, \lambda \in \mathbb{R}$

Conseguenza $F(\mu u+ \lambda v)=\mu F(u)+ \lambda F(v)$


**prep**: Siano $V,W$ spazi vettoriali, $F: V \to W$ è un applicazione lineare allora $F(\underline{0}_v)=\underline{0}_w$

<details>
<summary>
dimostrazione
</summary>

$F(0_v)=F(0 \times 0_v)=0 F(0_v)=0_w$

</details>

**Teorema 5.1.7** Siano V e W due spazi vettoriali. Se $v_1,\dots,v_n$ è una base di V e consideriamo n vettori $w_1,\dots,w_n \in W$ non necessariamente distinti, allora esiste ed è unica un' applicazione lineare $L:V\to W$ tale che $L(v_1)=w_1,\dots,L(v_n)=w_n$


## Assegnare un applicazione lineare

$F: \mathbb{R} \to \mathbb{R}^m$

1. $F(x_1,\dots,x_n)=(\dots)$
2. $F(e_1)=\dots, \dots,F(e_n)=\dots$
3. Assegnamo $A \in M_{m * n }(\mathbb{R})$


<details>
<summary>
esempio
</summary>

Primo modo:   
$(5e_1+3e_2, ,-e_2, e_1-e_2)$


Secondo modo   

$F(e_1)=5e_1+3e_2$
$F(e_2)=-e_2$
$F(e_3)=e_1-e_2$


Terzo modo   

$A= \begin{pmatrix} 5 & 0 & 1 \\ 3 & -1 & -1 \end{pmatrix}$

</details>


**Def**: Sia F $V \to W$ applicazione lineare 
$Im \space F= \{F(v)| v\in V\} \subseteq W$
$\ker F= \{v\in V|F(v)=\underline{0}\} \subseteq V$


**Prop**: $\ker F$ sottospazio di V, $Im \space F$ è sottospazio di $W$

**Dim**: $0_v \in \ker F$  perchè $F(0_v)=0_w$



**Prop** Sia $F V \to W$ applicazione lineare:
1. F è surrettiva $\iff Im \space F =W$
2. F è iniettiva $\iff \ker  F =\{\underline{0}\}$

> Nota $\{\underline{0}\}$ ha dim 0, una sua base è $\emptyset$
> Un sottospazio di dim 1 è del tipo $\{\lambda u |\lambda \in \mathbb{R}\}$ con $u \neq \underline{0}=<u>$ 


<details>
<summary>
dim
</summary>
	

Supponiamo che F è iniettiva mostriamo che $\ker F =\{\underline{0}\}$ ricordiamo che F è iniettiva se $F(u)=F(v)\implies u=v$

</details>



## Calcolo del nucleo 

$F:\mathbb{R}^n  \to \mathbb{R}^m$

$\ker F=\{x\in \mathbb{R}^n|F(x)=\underline{0}\}$

Sia A matrice associata ad F

cioè $F=L_a$ cioè $F(x)=Ax$, $\ker F=\{x\in \mathbb{R}^n | A x= \underline{0}\}$


Quindi $\ker F$ è l'insieme delle soluzioni del sistema lineare omogeneo associato ad A


<details>
<summary>
esmpio
</summary>

Sia $F :\mathbb{R}^3 \to \mathbb{R}^3$ definita da:
- $F(e_1)=e_1-e_2+2e_3=(1,-1,2)$
- $F(e_2)=e_1+e_2-e_3=(1,1,-1)$
- $F(e_3)=2e_2+e_3=(2,0,1)$


$A=\begin{pmatrix}F(e_1) & F(e_2) &F(e_3) \\\ 1 & 1 & 2 \\ 1 & 1 &0 \\ 2 & -1 & 1\end{pmatrix}$


$\ker F={x \in \mathbb{R}^3| F(x)=\underline{0}}$= ${x \in \mathbb{R}^3| A x= \underline{0}}$


</details>


**Prep** $F:V\to W$ applicazione lineare. Sia $\beta = \{v_1,\dots,v_n\}$ di base V allora $Im \space F =< F(v_1),\dots,F(v_n)>$



## Teorema della dimensione


Sia $F:V \to W$ applicazione lineare, allora $\dim V=\dim \ker F+ \dim Im \space F$








