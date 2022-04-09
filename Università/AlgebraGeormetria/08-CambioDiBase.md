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
> 
