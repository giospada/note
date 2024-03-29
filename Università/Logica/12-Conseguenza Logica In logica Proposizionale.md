# Conseguenza Logica

## Conseguenza Logica 
$\Gamma \Vdash F$ (conseguenza logica) quando per ogni mondo v si ha che, $\llbracket  G\rrbracket^v=1$ per ogni $G \in \Gamma$, allora $\llbracket  F\rrbracket^v=1$

Riscritta:
$\Gamma \Vdash F \iff \forall v(\forall G \in \Gamma, \llbracket G\rrbracket^v =1)\implies \llbracket  F\rrbracket^v =1$


## Equivalenza 

Come già anticipato:  
$F \equiv G$ quando $F \Vdash G$ e $G \Vdash F$  
Oppure si può dire:  
$F \equiv G$ quando per ogni mondo v , $\llbracket  F\rrbracket^v = \llbracket  G\rrbracket^v$


Nella logica **classica** si può anche dire:  

F e G sono logicamente equivalenti $F \equiv G$ quando **le loro tabelle diverità sono identiche**

<details>
<summary>
esempio
</summary>

![](vx_images/1099714806916.png)
</details>


### Tabella di verità 

$\Gamma \Vdash F$  è rappresentabile con tabelle di verità, ma solo se $\Gamma$ è un insieme finito

<details>
<summary>
Importante
</summary>

![](vx_images/442124002817000.png)

</details>

![](vx_images/5947726596008.png)



## Tautologica 

> F è tautologica quando $\Vdash F$ (F è conseguenza logica dell'insieme vuoto)

<details>
<summary>
esepio
</summary>

la tabella ha soli uno

$A\implies A$

![](vx_images/4869135239393.png)

</details>


## Soddisfacibile 

> F è soddisfacibile quando esiste un mondo v tale che $v \Vdash F$

<details>
<summary>
esepio
</summary>

la tabella ha almeno un uno

$\neg A$

</details>

> F è insoddisfacibile in un mondo v ($v \Vdash F$) sse $v(F)=1$

<details>
<summary>
esempio
</summary>

è insoddisfacibile se la tabella ha soli zero 

$A \wedge \neg A$

</details>


## Sostituzione


> Per Sostituire una formula G al posto di A in F scriviamo F[G/A]


![](vx_images/1891936219394.png)


> Teorema di invarianza per sostituzione: per tutte le formule $F,G_1,G_2$ e per ogni A, se $G_1 \equiv G_2$ allora $F[G1/A] \equiv F[G_2/A]$

<details>
<summary>
dimostrarzione 
</summary>

![](vx_images/324474819259397.png)
![](vx_images/590965001816920.png)
</details>

