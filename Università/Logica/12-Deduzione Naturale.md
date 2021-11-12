# Deduzione Naturale


![](vx_images/165632139381.png)

Per dimostrare si utilizza un **albero di deduzione naturale** per $\Gamma \vdash F$ è una struttura dati arorescente tale che :  
-  i nodi sono etichettati con delle formule
- le foglie sono formule [G]  ipotesi locali oppure formule non scartate G ipotesi globali
- la radice è etichettata con F
- le foglie non scaricate sono etichette con formule appartenenti a $\Gamma$
- i nodi interni, oltre alla formula sono etichettati con delle regole di inferenza

## Regloa Di Inferenza

Sintassi per la regloa di inferenza:

$\frac{F_1... F_n}{F}$

La formula F è la conclusione della regola.
Le formule $F_1\dots F_n$ sono le premesse della regola.

La premessa $F_i$ verrà indicata con $\displaylines{[A]\\ \vdots \\ F_i}$ per indicare che è possibile assumere localmente A per concludere $F_i$

Una regola senza premesse (n=0) si dice **assioma**.


Regole di introduzione: rispnde alla domanda **come concludo ?**
Regole di elminazione: rispnde alla domanda **cosa ricavao da ?**

1. Bottom-up (dalle premesse alla conclusione) date le premesse $F_1\dots F_n$ posso concludere F
2. Top-down (dalle premesse alla conclusione) per concludere F posso ridurmi a dimostrare $F_1\dots F_n$



## And $\wedge$

### Eliminazione And

#### Regola Unica



## Derivabilità

> un insieme di regole $R$ è derivabile a partire da un insieme di regole $S$ quando per ogni regola in $R$ le cui premesse sono $F1, . . . , Fn$ e la cui conclusione è $F$ si ha $F_1, . . . , F_n \vdash F$ usando solamente le regole in $S$

## Or $\vee$

## Introduzione


$\frac{F_1}{F_1\vee F_2}$

$\frac{F_1}{F_1\wedge F_2}$

**Non è Invertibile **

<details>
<summary>
A or Not A
</summary>

$\Vdash A \vee \neg A \mbox{ sse } \forall v \llbracket A \vee \neg A \rrbracket^v=1$   
$\mbox{ sse } \forall v \max\{v(A),1-v(A)\}=1$  
verificata

</details>


### Regola Di Eliminazione


## Bottom $\bot$

### Regola di eliminazione 

$\frac{\bot}{F}$

**Bottom-up**:dal falso seguie qualunque cosa
**Top-Down**: per dimostrare qualunque cosa  ridurmi a dimostrare un assurdo



## Top $\top$

### Introduzione 

$\frac{}{\top}$

è un assioma

### Regola di eliminazione


## Implicazione $\implies$

### Introduzione 

### Eliminazione

$\frac{F_1 \implies F_2, F_1}{F_2}$

