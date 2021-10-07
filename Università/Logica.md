---
header-includes: |
            \usepackage{mathtools}
---


# Docente

Claudio Sacerdoti Coen

![foto del professore con la giaguaro](img/proftigre.png)

# Logica

viene studiata da più discipline (fisica, matematica,informatica)

Domande chiave:
- cos'è la correttezza di un ragionamento?(e scriverlo in modo algoritmico)
- quali ragionamenti sono corretti?
- ci sono fatti non deducibili tramite un ragionamento?

la logica non parla di verità (più ragionamenti corretti)


# Paradossi

> Antinomia: è una conclusione inaccettabile,che deriva da premesse accettabili per mezzo di un ragionamento accettabile 

> Paradosso : conclusione contraria all'intuizione che deriva da premesse accettabili per mezzo di un ragionamento accettato (è accettabile)



<details>
    <summary>
    es falso paradosso
    </summary>

$x=1$  
$x^2=x$   
$x^2-1=x-1$  
$(x-1)(x+1)=x-1$  
$x+1=1$  
$x=0$  
</details>


## Linguaggio naturale

Il linguaggio naturale è alla base della comunicazione e del ragionamento umano, e per questo deve essere espressivo e viene esteso e specializzato (per comunicare )

Non possiamo utilizzarlo per procedure di calcolo e dimostrazioni perché:
- è ambiguo
- Fortemente dipende del contesto

<details>
    <summary>
    es
    </summary>

"la vecchia porta la sbarra" può essere interpretata in più volte

"lucia ha perso la testa..." è fortemente dipendente dal contesto

il linguaggio naturale non è adatto per le procedure di calcolo perché può avere più interpretazioni

```
if la vecciha porta la sbarra then
    amputa(gamba,dx)
else
    amputa(gamba,dx)
```

</details>
    
<details>
    <summary>
    es.1
    </summary>


"io mento"  

io mento se e solamente se cio che dico non ` e vero `  

io mento se e solamente se “io mento” non e vero `  

**io mento se e solamente se io non mento**

</details>

<details>
    <summary>
    es.2
    </summary>

Aggettivo autologico = aggettivo che si applica a se stesso (p.e. polisillabico)  
Aggettivo eterologico = aggettivo che non si applica a se stesso (p.e. monosillabico)  

“Eterologico e eterologico”  
eterologico e eterologico sse non si applica a se stesso `
**eterologico e eterologico sse eterologico non ` e eterologico**

</details>

i paradossi dei linguaggi naturali esistono perchè:
- l'uso meta-linguistico del linguaggio natruale
- l'auto-applicazione di un concetto meta-linguistico a se stesso
- l'uso della negazione per concludere qualcosa e la sua negazione

per evitare i paradossi bisogna impedire l'uso meta-linguistico del linguaggio naturale (**per questo si abbandona il linguaggio naturale per uno artificiale**)

## Linguaggio matematico

è che rientrino i paradossi

nel 1900 la matematica viene ristrutturata dalle basi, per farlo ricostruiscono tutta la matematica partendo con la teoria degli insiemi.  
la teoria degli insiemi parte dal presupposto che tutto è un insieme

### Paradosso di Russell

Russel è il primo a trovare un paradosso alla base della teoria degli insiemi.  
Essendo che tutto è un insieme si può utilizzare il simbolo di appartenenza tra oggetti.

**Paradosso**

> se x è un insieme che contiene tutti gli insiemi che non contengono se stessi  
> $X =\{ Y| Y \notin  Y\}$  
> $X \in X \text{ sse } X \notin X$

per ovviare al paradosso:
- non è possibile formare liberamnete un insieme per una proprietà 
- ma è possibile selezionare elementi da un insieme esistente 
- la collezione di tutti gli insiemi non è un insieme

[More](#teoria-assiomatiche-degli-insiemi)

## I paradossi in informatica

nella programmazione ogni linguaggio può eseguire delle funzioni che possono prendere in input e dare in output altre funzioni

supponiamo che le funzioni scrivibili in un linguaggio di prograzione dato un input, restituiscano un output in tempo finito

Sia `f(g) = not (g(g))`

allora `f(f)= not (f(f))`

pertanto:
- O f non è scrivibile in P è altamente inespressivo
- Oppure f non è totale (diverge, cioè non mi da nessun output in un tempo finito)

**Quindi le funzioni dei linguaggi di programmazione non sono funzioni matematiche**


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
- le **ripetizioni e l'ordine non contano** $\{1,2\} \text{\space\space è lo stesso insieme }  \{2,2,1,1\}$

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

$\forall X ,\forall Y ,(X = Y \Leftrightarrow \forall Z \text{ }(Z \in X \Leftrightarrow  Z\in Y ))$

per ogni insieme X e Y, X e Y sono uguali se e solo se per ogni Z appartiene a X e se e solo se Z appartiene a Y

### Definizione di essere sottoinsieme

> X è sottoinsieme di Y se Y possiede tutti gli elementi di X

$X \subseteq Y =^{def}= \forall Z, (X \in X \Rightarrow Z \in Y)$


definisco che X è sottoinsieme di Y quando per ogni Z , Z appartiene a X implica che Z appartiene a Y


### Assioma di separazione

> Dato un insieme, possiamo formare il sottoinsieme dei suoi elementi che soddisfano una proprietà

$\forall X ,\exists Y ,\forall Z ,(Z \in Y \Leftrightarrow Z \in X \wedge P (Z ))$

per ogni X esiste un Y, tutti gli insiemi in Z sono elementi di Y se sono appartenenti a X e hanno la proprietà

Abuso di notazione: $X =\{Y \in U| Y \notin Y\}$

> Attenzione: per descrivere Y c'è un abuso di notazione $\{Z \in X |P(Z)\}$ (Z è un elemento)

### Assioma dell’insieme vuoto

> L’insieme X viene indicato come $\emptyset$

$\exists X ,\forall Z ,Z \notin X$

### Definizione dell’insieme vuoto

> L’assioma è ridondante. Sia Y un qualunque altro insieme di cui un assoma asserisce l’esistenza (vedi p.e. assioma dell’infinito)

$\emptyset \coloneqq \{X \in Y |false\}$

### Definizione di intersezione binaria


$A \cap B \coloneqq \forall Z\{Z\in A |Z\in B\}$

**teorema**

$X \in A \cap B \Leftrightarrow X \in A \wedge X \in B$

### Definizione di intersezione

metto tutti gli insiemi da intersecare in F.

$\bigcap F \coloneqq \{ X \in A | \forall Y (Y \in F \Rightarrow X/Right \in Y) \}, A \in F$

### Assiome dell'unione binaria

$\forall A,\forall B,\exists X ,\forall Z ,(Z \in X \Leftrightarrow Z \in A \vee Z \in B)$

### Assioma dell'unione 

$\forall F \exists X \forall Z (Z\in X \Leftrightarrow \exists Y (Y \in F \wedge Z \in Y))$



### 4.2.10 Assioma del singoletto

$\forall X, \exists Y \forall Z (Z \in Y \Leftrightarrow Z = X)$

l'insieme Y viene indicato come {X}

> grazie a questo insieme possiamo creare un infinità di insiemi  
> es
> possiamo creare infiniti insiemi partendo da $\emptyset$ divente $\{\emptyset\}$  e combinato con l'unione si possono unire questi insiemi 

**(Abuso di) notazione**
Con la notazione $\{A_1, . . . , A_n\}$ indicheremo l’insieme $\{A_1\} . . .  \{A_n\}$ che esiste in virtu degli assiomi del singoletto è dell’unione.

TODO: finire al notazione matematica

### Assioma dell’infinito
Esiste un insieme che contiene almeno tutti (gli encoding de)i numeri naturali.

$\exists Y( \emptyset \in Y \wedge \forall N (N \in Y \Rightarrow N \cup \{N\} \in Y))$

Indichiamo temporaneamente con N tale insieme 



### Teorema esistenza di $N$

combinaimo altri assiomi con quello dell'infinito si arriva a dimostrare l'esistenza dell'insmieme N  che contiene tutti e soli i numeri naturali.

### Assioma dell'insieme potenza

Esiste l'insieme dei sottoinsiemi di un inseme dato.

$\forall \exists Y, \forall Z ( Z \in Y \Leftrightarrow Z \subseteq X$

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

$[0] \coloneqq \emptyset$  
$[n+1] \coloneqq [n] \cup \{[n]\}$

> esempi
> 

# Dimostrazioni


> regole di introduzione: sono quelle da utilizzare se voglio lavorare sulla conclusione, servono per introdurre una dimostrazione

> regole di eliminazione: servono per lavorare sull'ipotesi, la utilizziamo quando noi sappiamo già qualcosa

> postulato(o assioma):sono delle ipotesi che diamo per vere

> assioma: è un ipotesi che diamo per vera da quel momento in avanti

> enunciato di un teorema e ci  o che vogliamo dimostrare. Si compone di un insieme di ipotesi e di una conclusione


ogni passaggio va a lavorare su:
- le ipotesi
- la conclusione: che è quello che vogliamo andare a dimostrare in un determinato momento

## Per Ogni $\forall$

**introduzione**:Per dimostrare $\forall x P(x)$ (per ogni x vale P(x))

> “sia x (un insieme) fissato; . . .”   
> (i “. . .” sono una prova di P(x))

**eliminazione**:Per ogni ipotesi o risultato intermedio $\forall x P(x)$ potete concludere che P valga ciò che volete

## Implicazione $\Rightarrow$

**introduzione**: Per dimostrare $P \Rightarrow Q$

> “Assumo P (H). . . .”
> (“H”) e il nome dell’ipotesi; `
> i “. . .” sono una prova di Q)


**eliminazione**: Da un’ipotesi o un risultato intermedio $P \Rightarrow Q$ e da un’ipotesi o un risultato intermedio P potete concludere che Q vale.


**eliminazione** (variante): Da un’ipotesi o un risultato intermedio $P \Rightarrow Q$ di nome H , se volete concludere Q, potete procedere dicendo "per H , per dimostrare Q mi posso ridurre a dimostrare P" 


## Coimplica $\Leftrightarrow$

**introduzione**: Per dimostrare $P \Leftrightarrow Q$ allora devo dimostrare $P \Rightarrow Q$ e $Q \Rightarrow Q$

**eliminazione**:L'ipotesi $P \Leftrightarrow Q$ può essere usata sia come ipotesi $P \Rightarrow Q$ che come $Q \Rightarrow P$

## Espansione Definizioni

> **P ovvero Q**: serve per espandere P ottenendo la frase Q


## Regola della eliminazione dimostrazione

Da un ipotesi o un risltato intermetdio $p \Rightarrow Q$ di nome H, se volete concludere Q potete dire

## Regola dell'assurdo

Se attraverso le altre ipotesi rendono P falso, $P \Rightarrow assurdo$

## Congiunzione

**introduzione**: per dimostrare $P \wedge Q$: P e Q , si dimostrano sia P che Q

**eliminazione**:per eliminazione, può essere usato sia P che Q. in alternativa invece di concludere o assumere $P \wedge Q$ si può direttamente concludere o assumere $P (H_1)$ e $Q (H_2)$.

## Disginuzione

**introduzione**: per dimostrare $P \vee Q$ basta dimostrare P oppure Q dichiarandolo   
> "dimostro P" oppure "dimostro Q"

**eliminazione**:Data un’ipotesi o un risultato intermedio $P \vee Q$, si può proseguire nella dimostrazione per casi, una volta assumendo
che P valga e una volta che Q valga:
> “procedo per casi:  
> caso in cui valga P (H ): . . .  
> caso in cui valga Q (H ): . . . ”   


## Risultati intermedi

Potete anche utilizzare una **regola di introduzione** per dimostrare un **nuovo risultato intermedio**, diverso dalla conclusione corrente, a cui date un nome per utilizzarlo in seguito, a patto che abbiate già a disposizione le **premesse** della regola

## esiste

## Abbreviazioni

- **per ogni tale che**:
> “sia x tale che P(x). . . .”
> abbrevia
> “sia x (un insieme) fissato; assumo P(x); . . . ”
> per dimostrare $∀x P(x) \Rightarrow Q(x)$

- **Da $H_1, . . . , H_n$**:
- **Quindi**:


# Coppie ordinate

> negli insiemi l'ordine non conta e nemmeno la numerosità degli elementi

**coppie ordinate**: Una coppia ordinata, invece, e formata da due componenti di cui uno e identificato come primo e l’altro come secondo. Due  coppie sono uguali sse lo sono rispettivamente il primo e il secondo elemento

**Una coppia non èl'insieme dei suoi elementi e non deve essere pensata come contenete i suoi elementi**


# Dimostrazioni matematiche



> **Teorema**: E’ una proposizione con la quale si vuole affermare che un enunciato sia vero. Solitamente si presenta nella forma A,B,C,D… -> T, dove A,B,C,D sono le ipotesi e T la tesi.



