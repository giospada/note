# Teoria degli Insiemi

punti informali:  
- **tutto è un insieme**: gli insiemi contengono insiemi
- **è il linguaggio macchina** della matematica moderna, (tutto viene implementato come insiemi, es. numeri, figure geometriche)
- **è estremamente efficace nel farlo**: si riesce a descrivere ogni cosa, ma è difficilmente rappresentabili 
- permette di **introdurre e comprendere concetti come gli infiniti**
- si perdono gli aspetti computazionali (le funzioni definite come insiemi non si calcolano, le rappresentazioni di dati sono inefficienti ) 

## Teoria naive

> Attenzione:è inconsistente in quando si può avere il paradosso di Russell

- posso formare insiemi in **qualunque modo**
- gli insiemi **non devono essere omogenei**
- operazione base $\in$
- le **ripetizioni e l'ordine non contano** $\{1,2\} \text{  è lo stesso insieme }  \{2,2,1,1\}$

Come abbiamo visto il [paradosso di Russell](#paradosso-di-russell) crea un inconsistenza logica nella teoria naif.  
Per questo serve una teoria che rimuova l'**assioma di comprensione**(per ogni proprietà P si può creare un insieme $\{x | P(x)\}$), e che controlli l'uso meta-linguistico

> Attenzione: quando si usano insiemi rappresentanti altri insiemi, non si possono utilizzare i diagrammi di venn


## Teoria assiomatiche degli insiemi 

In una teoria assiomatica degli insiemi:  
- i concetti di **insieme, appartenenza e uguaglianza** non vengono definiti (gli insiemi sono **enti primitivi**)
- usiamo assiomi per asserire l'esistenza di alcuni insiemi a partire da altri
- ci sono numerose teorie insiemistiche che differiscono riguardo agli assiomi
- Noi seguiamo la teoria Zermelo-Fraenkel è la meno controversa, ed è sufficiente per sviluppare la maggior parte della matematica
- Zermelo Fraenkel non è mai stata dimostrata essere consistente (e non si è dimostrato che è dimostrabile che una teoria possa essere costistente)

### Assioma di estensionalità

> Due insiemi sono uguali sse hanno gli stessi elementi.  

$\forall X ,\forall Y ,(X = Y \iff \forall Z \text{ }(Z \in X \iff  Z\in Y ))$

per ogni insieme X e Y, X e Y sono uguali se e solo se per ogni Z appartiene a X e se e solo se Z appartiene a Y

### Definizione di essere sottoinsieme

> X è sottoinsieme di Y se Y possiede tutti gli elementi di X

$X \subseteq Y =^{def}= \forall Z, (X \in X \implies Z \in Y)$


definisco che X è sottoinsieme di Y quando per ogni Z , Z appartiene a X implica che Z appartiene a Y


### Assioma di separazione

> Dato un insieme, possiamo formare il sottoinsieme dei suoi elementi che soddisfano una proprietà

$\forall X ,\exists Y ,\forall Z ,(Z \in Y \iff Z \in X \wedge P (Z ))$

per ogni X esiste un Y, tutti gli insiemi in Z sono elementi di Y se sono appartenenti a X e hanno la proprietà

Abuso di notazione: $X =\{Y \in U| Y \notin Y\}$

> Attenzione: per descrivere Y c'è un abuso di notazione $\{Z \in X |P(Z)\}$ (Z è un elemento)

### Assioma dell’insieme vuoto

> L’insieme X viene indicato come $\emptyset$

$\exists X ,\forall Z ,Z \notin X$

### Definizione dell’insieme vuoto

> L’assioma è ridondante. Sia Y un qualunque altro insieme di cui un assoma asserisce l’esistenza (vedi p.e. assioma dell’infinito)

$\emptyset {:=} \{X \in Y |false\}$

### Definizione di intersezione binaria


$A \cap B {:=} \forall Z\{Z\in A |Z\in B\}$

**teorema**

$X \in A \cap B \iff X \in A \wedge X \in B$

### Definizione di intersezione

metto tutti gli insiemi da intersecare in F.

$\bigcap F {:=} \{ X \in A | \forall Y (Y \in F \implies X/Right \in Y) \}, A \in F$

### Assiome dell'unione binaria

$\forall A,\forall B,\exists X ,\forall Z ,(Z \in X \iff Z \in A \vee Z \in B)$

### Assioma dell'unione 

$\forall F \exists X \forall Z (Z\in X \iff \exists Y (Y \in F \wedge Z \in Y))$

### 4.2.10 Assioma del singoletto

$\forall X, \exists Y \forall Z (Z \in Y \iff Z = X)$

l'insieme Y viene indicato come {X}

> grazie a questo insieme possiamo creare un infinità di insiemi,
> possiamo creare infiniti insiemi partendo da $\emptyset$ divente $\{\emptyset\}$  e combinato con l'unione si possono unire questi insiemi 

**(Abuso di) notazione**
Con la notazione $\{A_1, . . . , A_n\}$ indicheremo l’insieme $\{A_1\} \cup . . . \cup \{A_n\}$ che esiste in virtu degli assiomi del singoletto è dell’unione.

$X \in \{A_1,...,A_n\}$ sse $X=A_1$ oppure ... oppure $X=A_n$ .

### Assioma dell’infinito
Esiste un insieme che contiene almeno tutti (gli encoding de)i numeri naturali.

$\exists Y( \emptyset \in Y \wedge \forall N (N \in Y \implies N \cup \{N\} \in Y))$

Indichiamo temporaneamente con N tale insieme 



### Teorema esistenza di $N$

combinaimo altri assiomi con quello dell'infinito si arriva a dimostrare l'esistenza dell'insmieme N  che contiene tutti e soli i numeri naturali.

### Assioma dell'insieme potenza

Esiste l'insieme dei sottoinsiemi di un inseme dato.

$\forall \exists Y, \forall Z ( Z \in Y \iff Z \subseteq X$

per ogni insieme X esiste un Y tale per cui, ogni Z elemento di Y se e solo se Z è un sottoinsieme di X

abuso di notazioni:$2^x$ oppure $P(x)$

> es  
> $2^{\{1,2\}}= \{\emptyset, \{1\},\{2\},\{1,2\}\}$  

### Assioma di regolarita (non da studiare) 

Ogni insieme non vuoto ha un elemento dal quale e disgiunto (senza elementi in comune ).Fra le conseguenze: nessun insieme contiene (ricorsivamente) se stesso e ha quindi senso cercare di misurare la taglia (chiamata cardinalita) di un insieme.

$A=\{\emptyset , \{ \emptyset\}\}$

$\emptyset \in A$ 
$\emptyset \cup A = \emptyset$ 

a e l'insime vouto soon disgiunti

### Assioma di rimpiazzamento

Intuitivamente: l’immagine di un insieme rispetto a una formula che descrive una funzione e ancora un insieme. Intuitivamente: se A e un insieme, quindi  e abbastanza piccolo, e a ogni elemento ne associo un altro, in una relazione molti-a-uno, quello che ottengo come immagine e ancora piccolo.



## Costruzioni dei Numeri Naturali

Assumo di avere i numeri reali con la mia meta matematica e li codifico con i miei insiemi

$\llbracket 0 \rrbracket {:=} \emptyset$  
$\llbracket n+1 \rrbracket {:=} \llbracket n \rrbracket \cup \{\llbracket n \rrbracket \}$

> esempi
> $\llbracket 0 \rrbracket =\emptyset$
> $\llbracket 1 \rrbracket =\{\emptyset\}$
> $\llbracket 2 \rrbracket =\{\emptyset,\{\emptyset\}\}$
> $\llbracket 3 \rrbracket =\{\emptyset,\{\emptyset\}\,\{\emptyset,\{\emptyset\}\}\}$
