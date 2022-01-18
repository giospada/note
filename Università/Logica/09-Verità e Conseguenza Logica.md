# Verità e Conseguenza Logica

## Verità

> Verità fisiche, chimiche... sono associate al mondo sensibile, e sono definite da esperimenti ripetibili

Cosa resta della verità quando manca il mondo sensibile?(matematica,informatica)

In una **teoria matematica**:  
- si creano degli **assiomi** che sono delle leggi che supponiamo valere nei mondi sotto considerazione.
- Un **modello matematico** della teoria è un qualunque mondo in cui interpretare i concetti matematici primitivi in modo tale che ogni assioma della teoria valga
- un **mondo** è una descrizione completa che determina un concetto di verità, gli assiomi individuano una molteplicità di mondi
- data una **preposizione** potrebbe essere sicuramente vera/falsa/non determinata in ogni modello della teoria.


### Esempio Teoria
Enti primitivi: $0,\space\le$  

Assiomi: $\le$ ha le proprietà riflessiva, antisimmetrica, transitiva e $\forall\space n,\space0\le n$.

Proposizioni:  
- $\forall\space x.x\le0\Rightarrow x=0$
- $\forall x,y.x\le y\vee y\le x$

<details>
<summary>
Modello 1
</summary>

interpreto gli oggetti come numeri naturali
0 come numero 0
≤ come ≤ sui naturali
tutti gli assiomi sono soddisfatti
entrambe le proposizioni sono vere
</details>

<details>
<summary>
Modello 2
</summary>

interpreto gli oggetti come numeri naturali
0 come numero 1
≤ come “divide”
tutti gli assiomi sono soddisfatti
solo la prima proposizione e vera
</details>


## Conseguenza Logica

> **Conseguenza Logica**: se una preposizione assume lo stesso valore di **verità in tutti i mondi**/modelli della teoria ($\Vdash$)

Sia $\Gamma$ un **insieme di sentenze** (costituiscono dei vincoli che i mondi devono rispettare) e F **una preposizione**.  
**F è conseguenza logica  di** $\Gamma (\Gamma \Vdash F)$ quando **F è vera in tutti i modelli di** $\Gamma$ ( ovvero tutti i mondi in cui ognuna delle $G \in \Gamma$ è vera).


## Equivalenza Logica

Siano F e G due sentenze, F è **logicamente equivalente** a G (si scrive $F \equiv G$) sse $F \Vdash G \mbox{ e } G \Vdash F$



## Teoria Inconsistente

> Una teoria è **inconsistenze** quando non ammette modelli, ovvero **nessun mondo tutti gli assiomi sono contemporaneamente veri.**


**se $\Gamma$ è inconsistente allora $\forall F$ si ha $\Gamma \Vdash F$**.

Se $\Gamma$ è inconsistente vale anche l'assurdo (se riesco a dimostrare l'assurdo $\Gamma$ è inconsistente).


<details>
<summary>
crollario
</summary>

Corollario: se $\Gamma$ è   inconsistente allora $\Gamma \Vdash \bot$ dove $\bot$ è una proposizione falsa (anche chiamata assurdo)
</details>
<details>


<summary>
Esempio
</summary>

$1=0,0\ne1,\forall x.x=x$ è una teoria inconsistente.

**Fatto ovvio:** $\Gamma$ inconsistente $\Rightarrow\forall F.\Gamma\Vdash F$.

**Dimostrazione:** $F$ deve valere nell'insieme vuoto dei modelli, il che è vero. 

**Corollario:** $\Gamma$ inconsistente $\Rightarrow\Gamma\Vdash\perp$, dove $\perp$ è una proposizione falsa, chiamata assurdo (anche l'assurdo è una conseguenza logica). Se è vero l'assurdo allora tutto il resto è vero.

Un teorema dice che è vero anche il contrario: $\Gamma\Vdash\perp\Rightarrow\Gamma$ è inconsistente, ovvero non ha modelli.

Tutte le teorie consistenti (= non consistenti, in cui l'assurdo non è conseguenza logica) sono interessanti. Esse hanno almeno un modello in cui tutte le conseguenze logiche di $\Gamma$ sono vere.
</details>