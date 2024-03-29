# Deduzione Naturale


## Introduzione

![](vx_images/165632139381.png)

Per dimostrare si utilizza un **albero di deduzione naturale** per $\Gamma \vdash F$ è una struttura dati arorescente tale che :  
-  i nodi sono etichettati con delle formule
- le foglie sono formule [G]  ipotesi locali oppure formule non scartate G ipotesi globali
- la radice è etichettata con F
- le foglie non scaricate sono etichette con formule appartenenti a $\Gamma$
- i nodi interni, oltre alla formula sono etichettati con delle regole di inferenza

### Correttezza

Una regola $\frac{F_1... F_n}{H}$ è corretta quando  $F_1,...,F_n \Vdash H$

$$\frac{ E \space\space\space\space \begin{matrix}
[F]\\
\vdots\\
G
\end{matrix}}{H}$$

Se contempla ipotesi allora si ha $E,F \implies G \Vdash H$

## Invertibilità

Una regola $\frac{F_1... F_n}{H}$ è **invertibile** quando per ogni i si ha  $H \Vdash F_i$, se scaricano delle ipotesi $H \Vdash G \implies F_i$ (queste regole sono importanti perchè può è essere applicata **senza portare a vicoli cechi**)

## Regola Di Inferenza

Sintassi per la regola di inferenza:

$\frac{F_1... F_n}{F}$

La formula F è la conclusione della regola.
Le formule $F_1\dots F_n$ sono le premesse della regola.

La premessa $F_i$ verrà indicata con $\displaylines{[A]\\ \vdots \\ F_i}$ per indicare che è possibile assumere localmente A per concludere $F_i$

Una regola senza premesse (n=0) si dice **assioma**.


Regole di introduzione: rispnde alla domanda **come concludo ?**
Regole di elminazione: rispnde alla domanda **cosa ricavao da ?**

1. Bottom-up (dalle premesse alla conclusione) date le premesse $F_1\dots F_n$ posso concludere F
2. Top-down (dalle premesse alla conclusione) per concludere F posso ridurmi a dimostrare $F_1\dots F_n$


## And ($\wedge$)

### Regole di introduzione

$\frac{F_1\space F_2}{F_1\wedge F_2}$
**Lettura bottom-up**: se $F_1$  e $F_2$ allora $F_1\wedge F_2$
**Lettura top-down**: per dimostrare $F_1\wedge F_2$ devo dimostrare sia $F_1$  che $F_2$.

<details>
<summary>
Scrittura informale:
</summary>


$...$ e quindi $F_1$

$...$ e quindi $F_2$

[e quindi $F_1\wedge F_2$]
</details>

<details>
<summary>
Correttezza classica: 
</summary>

$F_1,F_2\Vdash F_1\wedge F_2$ in quanto, $\forall v,\llbracket F_1\rrbracket^v=\llbracket F_2\rrbracket^v=1\implies\llbracket F_1\wedge F_2\rrbracket^v=min\{\llbracket F_1\rrbracket^v,\llbracket F_2\rrbracket^v\}=1$
</details>

<details>
<summary>
Invertibilità classica: 
</summary>

$F_1\wedge F_2\Vdash F_i$ per $I\in\{1,2\}$ in quanto, $\forall v,\llbracket F_1\wedge F_2\rrbracket^v=min\{\llbracket F_1\rrbracket^v,\llbracket F_2\rrbracket^v\}=1\implies\llbracket F_i\rrbracket^v=1$ per $I\in\{1,2\}$.
</details>


### Regola di eliminazione

$$\frac{ F_1\wedge F_2 \space\space\space \begin{matrix}
[F_1][F_2]\\
\vdots\\
F_3
\end{matrix}}{F_3}\space\space\space(\wedge_e)$$

**Lettura bottom-up**: se $F_1\wedge F_2$ e se ipotizzando $F_1$ e $F_2$ concludo $F_3$, allora $F_3$.
**Lettura top-down**: per dimostrare $F_3$ data l'ipotesi F1 ∧ F2 è sufficiente dimostrare $F_3$  sotto le ipotesi $F_1$ e $F_2$

<details>
<summary>
Scrittura informale:
</summary>

$. . . F_1 ∧ F_2$
[supponiamo $F_1$ e anche $F_2$]
$. . .$ e quindi $F_3$
[e quindi $F_3$]
L’applicazione della regola viene sempre lasciata implicita.
</details>

> Nota: un albero di derivazione che termini applicando la regola $∧_e$ ha due sotto-alberi immediati. Il primo dimostra $F_1 ∧ F_2$. Il secondo dimostra $F_3$ usando, fra le altre, le ipotesi $F_1$ e $F_2$  non ancora scaricate. è l’applicazione della regola che scarica le ipotesi dal sotto-albero.

La regola di eliminazione non è invertibile

$F_3=\top$ e $F_1,F_2=\bot$: si ha $\top\not{\Vdash}\bot\wedge\bot$

La regola è invertibile se si assume $F_1\wedge F_2$: ovvio in quanto $F_3\Vdash F_1\implies F_2\implies F_3$.

### Regole alternative di eliminazione

$\frac{F_1\wedge F_2}{F_1}\space\space(\wedge_{e1}),\space\space\space\space\frac{F_1\wedge F_2}{F_2}\space\space(\wedge_{e2})$

**Lettura bottom-up**: se $F_1\wedge F_2$ allora $F_1$ (e $F_2$).

**Lettura top-down**: per dimostrare $F_1$ (o $F_2$) basta dimostrare $F_1\wedge F_2.$

<details>
<summary>
Correttezza classica: 
</summary>

$F_1\wedge F_2\Vdash F_i$ per $i\in\{1,2\}$ in quanto in ogni mondo $v$ tale che $\llbracket F1 ∧ F2\rrbracket^v = min\{\llbracket F\rrbracket^v ,\llbracket F2\rrbracket^v \} = 1$ si ha $\llbracket Fi\rrbracket^v = 1$ per $i ∈ \{1, 2\}$.
</details>


## Or ($\vee$)

### Regole di introduzione

$\frac{F_1}{F_1\vee F_2}(\vee_{i_1})\space\space\frac{F_2}{F_1\vee F_2}(\vee_{i_2})$

**Lettura bottom-up**: se $F_1\space(F_2)$ vale, allora vale anche $F_1\vee F_2$

**Lettura top-down**: per dimostrare $F_1\vee F_2$ è sufficente dimostrare $F_1\space(F_2)$


<details>
<summary>
Correttezza Classica:
</summary>

 $F_i\Vdash F_1\vee F_2$ per $i\in\{1,2\}$ in quanto in ogni mondo $v$ tale che $\llbracket F_i\rrbracket^v=1$ si ha $\max\{\llbracket F_1\rrbracket^v,\llbracket F_2\rrbracket^v\}=1$
</details>

Le due regole **non sono invertibili**: per esempio $F_1=\bot$ e $F_2=\top$ si ha $\bot\vee\top\not{\Vdash}\bot$.

### Regole di eliminazione

$$\frac{F_1\vee F_2\space\space\begin{matrix}
[F_1]\\
\vdots\\
F_3
\end{matrix}\space\space\begin{matrix}
[F_2]\\
\vdots\\
F_3
\end{matrix}}{F_3}$$

**Lettura bottom-up**: se vale $F_1\vee F_2$ e $F_3$ vale sia quando vale $F_1$ che quando vale $F_2$, allora necessariamente $F_3$ vale.

**Lettura top-down**: per dimostrare qualunque cosa sapendo $F_1\vee F_2$ è sufficente per procedere per casi, dimostrando la stessa cosa assumendo prima che $F_1$ valga e poi che valga $F_2$

<details>
<summary>
Correttezza Classica:
</summary>

 si ha $F_1\vee F_2,F_1\implies F_3,F_2\implies F_3\Vdash F_3$ in quanto in ogni mondo $v$ tale che $\llbracket F_1\vee F_2\rrbracket^v=\max\{\llbracket F_1\rrbracket^v\}=1$ e $\llbracket F_1\implies F_3\rrbracket^v=\max\{1-\llbracket F_1\rrbracket^v,\llbracket F_3\rrbracket^v\}=1$ e $\llbracket F_F\implies F_3\rrbracket^v=\max\{1-\llbracket F_2\rrbracket^v,\llbracket F_3\rrbracket^v\}=1$ si ha $\llbracket F_3\rrbracket^v=1$. Il massimo vale sse c'è un $\llbracket F_i\rrbracket^v=1$ e in tal caso $1=\max\{1-\llbracket F_i\rrbracket^v,\llbracket F_3\rrbracket^v\}=\max\{0,\llbracket F_3\rrbracket^v\}=\llbracket F_3\rrbracket^v$
</details>

**Invertibilità**: la regola non è invertibile (controesempio: $F_3=\top$ e $F_1=F_2=\bot$). Tuttavia, quando $F_1\vee F_2$ è dimostrabile, allora la regola è banalmente invertibile.



### Armonia tra regole di introduzione ed eliminazione

$\frac{F_1\vee F_2\space\space\begin{matrix} [F_1]\\ \vdots\\ F_3 \end{matrix}\space\space\begin{matrix} [F_2]\\ \vdots\\ F_3 \end{matrix}}{F_3}$

- Ci sono due modi diretti per introdurre $F_1\vee F_2$ nel modo $i$-esimo si ha come premessa $F_i$. La regola di eliminazione analizza come la premessa $F_1\vee F_2$ viene ricavata. La regola ha 2 premesse: la $i$-esima assume $F_i$
- C'è un modo diretto per introdurre $F_1\wedge F_2$. Si ha come premesse $F_1$ e $F_2$. La regola di eliminazione analizza come la premessa $F_1\wedge F_2$ viene ricavata. La regola ha una premessa e assume sia $F_i$ che $F_2$


## Falso $\bot$

### Regola di eliminazione

$\frac{\bot}{F}$

**Lettura bottom-up**: dal falso segue qualunque cosa.

**Lettura top-down**: per dimostrare qualunque cosa posso ridurmi a dimostrare un assurdo

(Se le ipotesi sono false allora posso verificare qualsiasi cosa)


## Vero $\top$

### Regola di introduzione

$\frac{}{\top}$

**Lettura bottom-up**: il $\top$ è vero.
**Lettura top-down**: per dimostrare $\top$ non debbo fare nulla

## Implica $\implies$

### Regola di introduzione

$\frac{\displaylines{[F_1] \\ \vdots \\ F_2}}{F_1 \implies F_2}$


**Lettura bottom-up**: se ipotizzando $F_1$ dimostro $F_2$ allora $F_1\implies F_2$.

**Lettura top-down**: per dimostrare $F_1\implies F_2$ basta assumere $F_1$ e dimostrare $F_2$.

<details>
<summary>
Correttezza e invertibilità:
</summary>

 trivialmente $F_1\implies F_2\Vdash F_1\implies F_2$
</details>


### Regola di eliminazione

$\frac{F_1\implies F_2\space\space F_1}{F_2}$

**Lettura bottom-up**: se $F_1$ e $F_1\implies F_2$, allora necessariamente $F_2$.

**Lettura top-down**: per dimostrare $F_2$ debbo trovare un $F_1$ che valga e tale per cui $F_1\implies F_2$


## Negazione

Connetivo derivato $\neg F\equiv(F\implies\bot)$

Infatti in logica classica l'implicazione è vera sse 

1. la conclusione $\bot$ è vera in nessun mondo
2. la premessa $F$ è falsa ($\equiv F$ è vera)

Pertanto possiamo derivare le regole del $\neg$ come caso speciale di quelle dell' $\implies$.

Definiamo $\neg F_1$ come $F_1\implies\bot$ per ottenere le regole per il $\neg$ come istanze delle regole per l'$\implies$.

### Regola di introduzione
$\frac{\begin{matrix} [F_1]\\ \vdots\\ \bot \end{matrix}}{\neg F_1}\space(\neg_i)$

**Lettura bottom-up**: se ipotizzando $F_1$ dimostro l'assurdo allora  $\neg F_1$.
**Lettura top-down**: per dimostrare $\neg F_1$ basta assumere $F_1$ e dimostrare l'assurdo.

## Regole di eliminazione

$\frac{\neg F_1\space\space F_1}{\bot}\space\space(\neg_e)$

**Lettura bottom-up**: è assurdo avere sia $\neg F_1$ che $F_1$

**Lettura top-down**: per dimostrare l'assurdo basta dimostrare qualcosa e il suo contrario.

L'invertibilità per il $\neg$ segue da quella della regola per il $\implies_i$.

Inoltre, quando ci is trova a dimostrare il $\bot$, da quel momento in avanti tutte le regole applicabili sono invertibili in quanto la conclusione  $\bot$ ha come conseguenza logica qualunque formula. In ogni momento, dopo aver accumulato nuove ipotesi  e quando si è bloccati, è possibile tornare a dimostrare $\bot$ per mezzo della regola $\bot_e$. Infine, l'intuizione diventa spesso inutile (le ipotesi sono inconsistenti).

L'invertibilità per l' $\neg_e$ è ovvia in quanto $\bot\vdash F_1$ e $\bot\vdash\neg F_1$. La regola è comunque di difficile applicazione in quanto se non si sceglie l'$F_1$ giusto, si è solo duplicato il lavoro inutilmente. 



todo:da 45

## Teorema di Completezza 


ho aggiunto tute le regole che mi servono per catturare sintatticamente un concetto semantico


la deduzione naturale non è completa perchè non possiamo verificare le seguenti tautologie:
- $\Vdash \neg \neg A \implies A$
- $\Vdash \neg A \vee A$

le regole date finora non rendono il sistema completo per la logica proposizionale classica


## RAA

![](vx_images/4374204149395.png)


**Lettura bottom-up**: Assumiamo per assurdo $\neg F$. . . . Assurdo! Quindi F.
**Lettura top-down**: Per dimostrare F procediamo per assurdo assumendo $\neg F$ e dimostrando $\bot$.


> ATTENZIONE: Funziona solamente per la logica classica 

