
# Logica

## Preposizione

> p = proposizione (è un affermazione che può essere o vera o falsa)

## Negazione

$\bar{p}$ = "non p", è la negazione di p


### Per ogni e Esiste

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
</details>

## Inplicazione, Se e solo se

$p \implies q$ = "p implica q" (p si chiama ipotesi e q si chiama tesi)

Si può leggere "p condizione sufficente per q" oppure "q condizione necessaria per p".

<details>
    <summary>
        tabella di verità e equivalenza
    </summary>
    
| p | q |$p \implies q$| 
|---|---|---------------------|
| V | V |           V         |
| V | F |           F         |
| F | V |           V         |
| F | F |           V         

</details>


$p \iff q$ = "p implica q" 

significa che $(p \implies q) \wedge( q \implies q)$


<details>
    <summary>
        tabella di verità
    </summary>
    
| p | q |$p \iff q$| 
|---|---|---------------------|
| V | V |           V         |
| V | F |           F         |
| F | V |           F         |
| F | F |           V         |

</details>