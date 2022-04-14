# Cambio di Base

sia $F:V\to W$ lineare dove V e W sono spazi vettoriali

$\beta={v_1,\dots,v_n}$ base di V
$\beta'={w_1,\dots,w_n}$ base di W

Dove $\beta\beta'$ son basi ordinate

esiste una matrice $A_{\beta\beta'}\in M_{n,m}(\mathbb{R})$ tale che $(F(v))_{\beta'}=A_{\beta\beta'} \cdot (v)_\beta$


$A_{\beta\beta'}$ si dice la matrice associata ad $F$ rispetto alle basei $\beta$ (def dominio) e $\beta'$ (del codominio)

$A_{\beta\beta'}=\begin{pmatrix}F(v_1)_{\beta'}\dots F(v_n)_{\beta'}\end{pmatrix}$

Nella i-esima colonna di $A_{\beta\beta'}$ ci sono le coordinate di $F(v_i)$ rispetto alla base $\beta'$, dove $v_i$ è l'i-esimo vettore della base $\beta$

<details>
<summary>
dimostrazione
</summary>


TODO:

</details>





## Notazione

quando $V=W$ e $F=id$ e $\beta=\beta'=\mathbb{C}$

le matrici associate all'identità verranno indicate con $I_{\beta\beta'}$


**osservazione** $F:\mathbb{R}^n\to\mathbb{R}^m$, $\beta=\beta'=\mathbb{C}, A_{\mathbb{C}\mathbb{C}'}$ è proprio la solita $A$
quindi $(w)_{\mathbb{C}}=w$


> Nota: La composizione di applicazioni lineari, è compatibile per il prodotto righe per colonne con matrici anche nel aso di basi qualsiasi

## temp

Mtrice associata ad un applicazione lin $F: V \to W$ rispetto alle basi $\beta=\{v_1,\dots,v_n\}$ del dominio di $\beta'$ del codominio notazione $A_{\beta \beta'}=M_{\beta \beta'}(F)=\begin{pmatrix} F(v_1)_{\beta'} & \dots &F(v_n)_{\beta'}\\ \vdots &\vdots & \vdots \end{pmatrix}$ vale $(F(v))_{\beta'}=A_{\beta\beta'} \cdot (v)_{\beta}$ caso particolare $F= id, \mathbb{R}^n\to \mathbb{R}^n$ ,$\beta$ base $I_{\beta\beta}=M_{\beta\beta}(id)=\begin{pmatrix} 1& \dots &0 \\ \vdots & \vdots & \vdots \\ 0 &\dots &1 \end{pmatrix}$

F=id $\beta$ nel dominio $\mathbb{C}$ nel codominio $I_{\beta \mathbb{C}}=M_{\beta \mathbb{C}}(id)=\begin{pmatrix} v_1 & \dots & v_n \\ \vdots &\vdots & \vdots \end{pmatrix}$ , $\beta=\{v_1,\dots,v_n\}$ 



**Dim**: $\mathbb{R}^n_{\mathbb{C}} \to_{I_{C\beta}}$ $\mathbb{R}^n_{\beta}$ $\to_{I_{\beta C}}  \mathbb{R}^n_{\mathbb{C}}$ , $I_{\beta \mathbb{C}} I_{\mathbb{C}\beta}=I_{\mathbb{C}\mathbb{C'}}=I$ $=I_{\beta\beta}=I$

## Cambio di base 


sia $F: \mathbb{R}^n \longrightarrow \mathbb{R}R^m$ un'applicazione lineare, $A_{C,C'}$, la matrice ad essa associata rispetto alle basi canoniche $C, C'$ nel dominio e nel codominio rispettivamente.
Allora la matrice associata a $F$ rispetto alle basi $B$ nel dominio e $B'$ nel codominio è data da: $A_{B,B'}=I^{-1}_{B',C'}A_{C,C'}I_{B,C}$
dove:

- $A_{C,C'}$  ha per colonne le coordinate delle immagini dei vettori della base canonica, cioé di $F(e_1)...\ F(e_n)$ rispetto alla base canonica di $\mathbb{R}^m$
- $I_{B',C'}$ ha per colonne le coordinate dei vettori della base $B'$, rispetto alla base canonica di $\mathbb{R}^m$
- $I_{B,C}$ ha per colonna le coordinate dei vettori della base $B$, rispetto alla base canonica di $\mathbb{R}^n$



