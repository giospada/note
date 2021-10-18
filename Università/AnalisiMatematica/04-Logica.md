
# Logica

> p = proposizione (è un affermazione che può essere o vera o falsa)

$\bar{p}$ = "non p", è la negazione di p


attezione :
- la negazione di tutti è esiste almeno un elemento $\bar{\forall}$ = $\exists$  
- la negazioni di esiste almeno un elementeo è tutti  $\bar{\exists}$ = $\forall$

<details>
    <summary>
        esempi
    </summary>

es.
p = ogni elemento di A è un numero pari  
$\forall a \in A : \text{a è pari}$   
$\bar{p} = \exists a \in A : \text{a non è pari}$ 
</detailS>


$p \Rightarrow q$ = "p implica q" (p si chiama ipotesi e q si chiama tesi)

<details>
    <summary>
        tabella di verità e equivalenza
    </summary>
| p | q |$p \Rightarrow q$| 
|---|---|---------------------|
| V | V |           V         |
| V | F |           F         |
| F | V |           V         |
| F | F |           V         

</details>


$p \Leftrightarrow q$ = "p implica q" 

significa che $(p \Rightarrow q) \wedge( q \Rightarrow q)$

"è sufficiente p affinché q"

<details>
    <summary>
        tabella di verità
    </summary>
| p | q |$p \Leftrightarrow q$| 
|---|---|---------------------|
| V | V |           V         |
| V | F |           F         |
| F | V |           F         |
| F | F |           V         |

</details>