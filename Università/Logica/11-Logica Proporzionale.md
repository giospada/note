# Logica Proporzionale

La logica proprozionale studia solamente le connotazioni che denotano valori di verità.

## Sintassi

> $F::= \top |\bot|A|B|...|\neg F|F\vee F|F\wedge F|F \implies F$

Semantica intuitiva:  
- $\top$ denota la verità
- $\bot$ denota la falsità
- A,B,... Denotano un valore di verità non determinato o sconoscuto
- $\neg F$ è la negazione di F
- $F\vee F$  è la digiunzione inclusi di due formule 
- $F\wedge F$: 
- $F \implies F$:

Rendiamo la sintassi non ambigua:
- Precedenze: $\neg , \wedge,\vee,\implies$
- Associatività a destra


<details>
<summary>
Esempi
</summary>

TODO
</details>



## Formalizzazione 

> Con **formalizzazione** di una frase naturale si intende trovare la formula logica che meglio approssima la frase


<details>
<summary>
Esempi
</summary>

Se 2+2 fa 5 allora io sono una carriola

Formalizzazione: $A \implies B$
- A sta per "2+2 fa 5"
- B sta per "io sono una carriola"

------

Non è vero che quando fa caldo bisogna accednere il condizionatore

Formalizzazione: $\neg (A \implies B)$

</details>

## Semantica

> **Semantica**: ciò che viene associato alle connotazioni in un particolare 
> **dominio di interpretazione**; insieme delle denotazioni

La semantica classica: associa a ogni connotazione il suo **valore di verità** in un qualche mondo, sarà il **mondo a determinare** il vaolre di verità delle **variabili**.

- Ogni enunciato è vero o falso
- Un enunciato non può essere vero e falsoallo stesso tempo
- il valore di verità non muta
- il valore di verità di un enunciato è sempre determinato
- Staticità e determinanza segnano un solco fra verità e conoscenza
- Staticità segna un solco fra verità e risorse


Utilizziamo 0 e 1, per denotare la falsità e la verità

> un interpretazione o mondo è una fnzione delle insieme delle variabili proposizionali {A,B,....} verso {0,1}


![](vx_images/2567958149376.png)


## Dimostrazioni e Prove

Partendo da $\Gamma \vdash F$ 
