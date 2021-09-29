
- [1. Docente](#1-docente)
- [2. Logica](#2-logica)
- [3. Paradossi](#3-paradossi)
  - [3.1. Linguaggio naturale](#31-linguaggio-naturale)
  - [3.2. Linguaggio matematico](#32-linguaggio-matematico)
    - [3.2.1. Paradosso di Russell](#321-paradosso-di-russell)
  - [3.3. I paradossi in informatica](#33-i-paradossi-in-informatica)
- [4. Teoria degli Insiemi](#4-teoria-degli-insiemi)
  - [4.1. Teoria naive](#41-teoria-naive)
  - [4.2. Teoria assiomatiche degli insiemi](#42-teoria-assiomatiche-degli-insiemi)
    - [4.2.1. Assiomi](#421-assiomi)
    - [4.2.2. Definizione di intersezione binaria](#422-definizione-di-intersezione-binaria)
    - [4.2.3. Teorema](#423-teorema)
  - [4.3. Itersezione n-aria](#43-itersezione-n-aria)
    - [4.3.1. Definizione di intersezione](#431-definizione-di-intersezione)



# 1. Docente

Claudio Sacerdoti Coen

![foto del professore con la giaguaro](img/proftigre.png)

# 2. Logica

viene studiata da più discipline (fisica, matematica,informatica)

Domande chiave:
- cos'è la correttezza di un ragionamento?(e scriverlo in modo algoritmico)
- quali ragionamenti sono corretti?
- ci sono fatti non deducibili tramite un ragionamento?

la logica non parla di verità (più ragionamenti corretti)


# 3. Paradossi

> Antinomia: è una conclusione inaccettabile,che deriva da premesse accettabili per mezzo di un ragionamento accettabile 

> Paradosso : conclusione contraria all'intuizione che deriva da premesse accettabili per mezzo di un ragionamento accettato (è accettabile)


> postulato(o assioma):sono delle ipotesi che diamo per vere


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


## 3.1. Linguaggio naturale

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

## 3.2. Linguaggio matematico

è che rientrino i paradossi

nel 1900 la matematica viene ristrutturata dalle basi, per farlo ricostruiscono tutta la matematica partendo con la teoria degli insiemi.  
la teoria degli insiemi parte dal presupposto che tutto è un insieme

### 3.2.1. Paradosso di Russell

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

## 3.3. I paradossi in informatica

nella programmazione ogni linguaggio può eseguire delle funzioni che possono prendere in input e dare in output altre funzioni

supponiamo che le funzioni scrivibili in un linguaggio di prograzione dato un input, restituiscano un output in tempo finito

Sia `f(g) = not (g(g))`

allora `f(f)= not (f(f))`

pertanto:
- O f non è scrivibile in P è altamente inespressivo
- Oppure f non è totale (diverge, cioè non mi da nessun output in un tempo finito)

**Quindi le funzioni dei linguaggi di programmazione non sono funzioni matematiche**


# 4. Teoria degli Insiemi

punti informali:
- **tutto è un insieme**: gli insiemi contengono insiemi
- **è il linguaggio macchina** della matematica moderna, (tutto viene implementato come insiemi, es. numeri, figure geometriche)
- **è estremamente efficace nel farlo**: si riesce a descrivere ogni cosa, ma è difficilmente rappresentabili 
- permette di **introdurre e comprendere concetti come gli infiniti**
- si perdono gli aspetti computazionali (le funzioni definite come insiemi non si calcolano, le rappresentazioni di dati sono inefficienti ) 

## 4.1. Teoria naive

> Attenzione:è inconsistente in quando si può avere il paradosso di Russell

- posso formare insiemi in **qualunque modo**
- gli insiemi **non devono essere omogenei**
- operazione base $\in$
- le **ripetizioni e l'ordine non contano** $\{1,2\} \text{\space\space è lo stesso insieme }  \{2,2,1,1\}$

Come abbiamo visto il [paradosso di Russell](#paradosso-di-russell) crea un inconsistenza logica nella teoria naif.  
Per questo serve una teoria che rimuova l'**assioma di comprensione**(per ogni proprietà P si può creare un insieme $\{x | P(x)\}$), e che controlli l'uso meta-linguistico

> Attenzione: quando si usano insiemi rappresentanti altri insiemi, non si possono utilizzare i diagrammi di venn


## 4.2. Teoria assiomatiche degli insiemi 

In una teoria assiomatica degli insiemi:
- i concetti di **insieme, appartenenza e uguaglianza** non vengono definiti (gli insiemi sono **enti primitivi**)
- usiamo assiomi per asserire l'esistenza di alcuni insiemi a partire da altri
- ci sono numerose teorie insiemistiche che differiscono riguardo agli assiomi
- Noi seguiamo la teoria Zermelo-Fraenkel è la meno controversa, ed è sufficiente per sviluppare la maggior parte della matematica
- Zermelo Fraenkel non è mai stata dimostrata essere consistente (e non si è dimostrato che è dimostrabile che una teoria possa essere costistente)

### 4.2.1. Assiomi

**Assioma di estensionalità**  

> Due insiemi sono uguali sse hanno gli stessi elementi.  

$\forall X ,\forall Y ,(X = Y \Leftrightarrow ∀Z \text{ }(Z \in X \Leftrightarrow  Z\in Y ))$

> **Definizione di essere sottoinsieme**

 X è sottoinsieme di Y se Y possiede tutti gli elementi di X

$X \subseteq Y =^{def}= \forall Z, (X \in X \Rightarrow Z \in Y)$

**Assioma di separazione**

> Dato un insieme, possiamo formare il sottoinsieme dei suoi elementi che soddisfano una proprietà

$\forall X ,\exist Y ,\forall Z ,(Z \in Y \Leftrightarrow Z \in X \wedge P (Z ))$

TODO: non ho ben capito la parte di implicazione

**Assioma dell’insieme vuoto**

> L’insieme X viene indicato come ∅

$\exists X ,\forall Z ,Z \notin X$

**Definizione dell’insieme vuoto**

> L’assioma è ridondante. Sia Y un qualunque altro insieme di cui un assoma asserisce l’esistenza (vedi p.e. assioma dell’infinito)

### 4.2.2. Definizione di intersezione binaria

### 4.2.3. Teorema

Dimostraizone per l'assioma di separazione

## 4.3. Itersezione n-aria

grazie all'intersezione binaria posso intersecare un numero infinito di insiemi

### 4.3.1. Definizione di intersezione

> Dato un insieme di insiemi, esiste l’insieme che ne è l’intersezione

