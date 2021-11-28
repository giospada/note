# Logica Proporzionale

La logica proporzionale studia solamente le connotazioni che denotano valori di verità.

## Sintassi

> $F::= \top |\bot|A|B|...|\neg F|F\vee F|F\wedge F|F \implies F$

Semantica intuitiva:  
- $\top$ denota la verità
- $\bot$ denota la falsità
- A,B,... Denotano un valore di verità non determinato o sconosciuto
- $\neg F$ è la negazione di F
- $F\vee F$  è la disgiunzione inclusi di due formule 
- $F\wedge F$: 
- $F \implies F$:

Rendiamo la sintassi non ambigua:
- Precedenze: $\neg , \wedge,\vee,\implies$
- Associatività a destra



## Formalizzazione 

> Con **formalizzazione** di una frase naturale si intende trovare la formula logica che meglio approssima la frase


<details>
<summary>
Esempi
</summary>

1. Se 2+2 fa 5 allora io sono una carriola
    Formalizzazione: $A \implies B$
    - A sta per "2+2 fa 5"
    - B sta per "io sono una carriola"

2.Non è vero che quando fa caldo bisogna accendere il condizionatore, Formalizzazione: $\neg (A \implies B)$
</details>

Bisogna stare attenti a :  
1. **Connotazioni diverse per gli stessi connettivi** 
2. **Sinonimi e contrari** 

<details>
<summary>
Esempo connotazioni diverse:
</summary>

- “Se A allora B”, “A implica B”, “B se A”, “B quando A”,
“quando A, B”, “A è condizione sufficiente per B”, “B è
condizione necessaria per A”, . . .
- “A e B”, “A ma B”, “A nonostante B”, . . .
</details>

<details>
<summary>
Esempio Sinonimi e contrari:
</summary>

“se Mario è acculturato allora oggi c’è bel tempo”, “oggi
splende il sole e Mario è ignorante” si formalizza come
$M ⇒ B, B ∧ ¬M$
</details>

## Semantica

> **Semantica**: ciò che viene associato alle connotazioni in un particolare **dominio di interpretazione**; insieme delle denotazioni (la semantica determina il significato di un lingaggio)

### Semantica Classica

**La semantica classica:** associa a ogni connotazione il suo **valore di verità** in un qualche mondo, sarà il **mondo a determinare** il vaolre di verità delle **variabili**.

- Ogni enunciato è vero o falso
- Un enunciato non può essere vero e falso allo stesso tempo
- il valore di verità non muta
- il valore di verità di un enunciato è sempre determinato
- Staticità e determinatezza segnano un solco fra verità e conoscenza
- Staticità segna un solco fra verità e risorse


Utilizziamo 0 e 1, per denotare la falsità e la verità

> **Definizione**: una (funzione di) interpretazione (classica) o mondo è una funzione dall'insieme delle variabili proposizionali {A,B,...}verso {0,1}


- $\llbracket  \bot \rrbracket^v= 0$
- $\llbracket  \top \rrbracket^v = 1$
- $\llbracket  A \rrbracket^v =v(A)$
- $\llbracket  \neg F \rrbracket^v =1-\llbracket  F\rrbracket^v$
- $\llbracket  F_1 \wedge F_2 \rrbracket^v=\min \{\llbracket  F_1 \rrbracket^v, \llbracket  F_2 \rrbracket^v\}$
- $\llbracket  F_1 \vee F_2 \rrbracket^v=\max\{\llbracket  F_1 \rrbracket^v, \llbracket  F_2 \rrbracket^v\}$
- $\llbracket  F_1 \implies F_2 \rrbracket^v=\max\{1-\llbracket  F_1 \rrbracket^v, \llbracket  F_2\rrbracket^v\}$
