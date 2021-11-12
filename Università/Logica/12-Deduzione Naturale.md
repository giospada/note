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

