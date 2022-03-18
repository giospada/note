# AVL

È un albero bilanciato che mantiene l'altezza dell'albero così che tutte le operazioni abbiano costo algoritmico per le operazioni di `search`, `delete` e `insert` in $O(\log n)$n le caso pessimo.

> **Fattore di bilanciamento** β(v) di un nodo v è dato dalla differenza tra l’altezza del sottoalbero sinistro e destro di v: β(v) = altezza(v.left) - altezza(v.right)

> **Bilanciamento in altezza** se per ogni nodo v le altezze dei suoi sottoalberi sinistro e destro differiscono al più di uno $|\beta(v)|\le 1$


L'albero può essere **sbilanciato** dalle operazioni di insert e delete 

## Operazioni


**UpdateHeight**: TODO

**Beta**: TODO 

[finire pag 13](https://virtuale.unibo.it/pluginfile.php/1113437/mod_resource/content/5/07%20-%20Alberi%20AVL.pdf)

 **Rotazione semplice**:scambia il nodo radice mantenendo la proprietà di ordinamento dell'albero   
![](vx_images/260206600615204.png )

questa operazione costa `O(1)`

**Sbilanciamenti**:
- SS:$\beta(u)=2$ e $\beta(left(u))\ge 0$
- DD: $\beta(u)=-2$ e $\beta(right(u))\le 0$
- SD: $\beta(u)=2$e $\beta(right(u))=-1$

- DS:$\beta(u)=-2$e $\beta(right(u))= 1$

<details>
<summary>
Sbilanciamento SS
</summary>


si fa perno su u e si ruota v, rotazione a destra


![](vx_images/421803324940955.png)

</details>





<details>
<summary>
Sbilanciamento SD
</summary>


1. si fa perno su v e si fa una rotazione a SX
![](vx_images/486084188889359.png)

2. rotazione DX con perno su u

![](vx_images/310112717576001.png)

</details>