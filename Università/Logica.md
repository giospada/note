---
header-includes: |
            \usepackage{mathtools}
---

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
    - [4.2.1. Assioma di estensionalità](#421-assioma-di-estensionalità)
    - [4.2.2. Definizione di essere sottoinsieme](#422-definizione-di-essere-sottoinsieme)
    - [4.2.3. Assioma di separazione](#423-assioma-di-separazione)
    - [4.2.4. Assioma dell’insieme vuoto](#424-assioma-dellinsieme-vuoto)
    - [4.2.5. Definizione dell’insieme vuoto](#425-definizione-dellinsieme-vuoto)
    - [4.2.6. Definizione di intersezione binaria](#426-definizione-di-intersezione-binaria)
    - [4.2.7. Definizione di intersezione](#427-definizione-di-intersezione)
    - [4.2.8. Assiome dell'unione binaria](#428-assiome-dellunione-binaria)
    - [4.2.9. Assioma dell'unione](#429-assioma-dellunione)
    - [4.2.10. 4.2.10 Assioma del singoletto](#4210-4210-assioma-del-singoletto)
    - [4.2.11. Assioma dell’infinito](#4211-assioma-dellinfinito)
    - [4.2.12. Teorema esistenza di $N$](#4212-teorema-esistenza-di-n)
    - [4.2.13. Assioma dell'insieme potenza](#4213-assioma-dellinsieme-potenza)
    - [4.2.14. Assioma di regolarita (non da studiare)](#4214-assioma-di-regolarita-non-da-studiare)
    - [4.2.15. Assioma di rimpiazzamento](#4215-assioma-di-rimpiazzamento)
  - [4.3. Costruzioni dei Numeri Naturali](#43-costruzioni-dei-numeri-naturali)
- [5. Dimostrazioni](#5-dimostrazioni)
  - [5.1. Per Ogni $\forall$](#51-per-ogni-forall)
  - [5.2. Implicazione $\Rightarrow$](#52-implicazione-rightarrow)
  - [5.3. Coimplica $\Leftrightarrow$](#53-coimplica-leftrightarrow)
  - [5.4. Espansione Definizioni](#54-espansione-definizioni)
  - [5.5. Regola della eliminazione dimostrazione](#55-regola-della-eliminazione-dimostrazione)
  - [5.6. Regola dell'assurdo](#56-regola-dellassurdo)
  - [5.7. Congiunzione](#57-congiunzione)
  - [5.8. Disginuzione](#58-disginuzione)
  - [5.9. Risultati intermedi](#59-risultati-intermedi)
  - [5.10. esiste](#510-esiste)
  - [5.11. Abbreviazioni](#511-abbreviazioni)
- [Relazioni, Funzioni ...](#relazioni-funzioni-)
  - [Coppie ordinate](#coppie-ordinate)
    - [teorema di caratterizzazione delle coppie](#teorema-di-caratterizzazione-delle-coppie)
  - [Teorema del prodotto cartesiano tra gli insiemi](#teorema-del-prodotto-cartesiano-tra-gli-insiemi)
  - [Relazione](#relazione)
    - [Teorema: relazioni verso insiemi vuoiti](#teorema-relazioni-verso-insiemi-vuoiti)
  - [Dimostrazione Di Funzioni](#dimostrazione-di-funzioni)
    - [Teorema esistenza dello spazio di funzioni come insieme](#teorema-esistenza-dello-spazio-di-funzioni-come-insieme)
  - [Abbreviazioni](#abbreviazioni)
  - [Priorprietà delle relazioni](#priorprietà-delle-relazioni)
    - [Relazioni di ordinamento strette](#relazioni-di-ordinamento-strette)
    - [Relazioni di ordinamento lasche](#relazioni-di-ordinamento-lasche)
    - [Relazioni di equivalenza $\equiv$](#relazioni-di-equivalenza-equiv)
    - [Classi di equivalenza](#classi-di-equivalenza)
    - [Insieme quoziente](#insieme-quoziente)
    - [Costruzione di Z](#costruzione-di-z)
    - [Costruzione dei razionali](#costruzione-dei-razionali)
  - [iniettiva surrettiva biettività](#iniettiva-surrettiva-biettività)
  - [Cardinatlità](#cardinatlità)
    - [Teorema: esistenza dei numeri cardinali come insiemi](#teorema-esistenza-dei-numeri-cardinali-come-insiemi)
- [Insiemi infiniti](#insiemi-infiniti)
- [7. Dimostrazioni matematiche](#7-dimostrazioni-matematiche)

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

### 4.2.1. Assioma di estensionalità

> Due insiemi sono uguali sse hanno gli stessi elementi.  

$\forall X ,\forall Y ,(X = Y \Leftrightarrow \forall Z \text{ }(Z \in X \Leftrightarrow  Z\in Y ))$

per ogni insieme X e Y, X e Y sono uguali se e solo se per ogni Z appartiene a X e se e solo se Z appartiene a Y

### 4.2.2. Definizione di essere sottoinsieme

> X è sottoinsieme di Y se Y possiede tutti gli elementi di X

$X \subseteq Y =^{def}= \forall Z, (X \in X \Rightarrow Z \in Y)$


definisco che X è sottoinsieme di Y quando per ogni Z , Z appartiene a X implica che Z appartiene a Y


### 4.2.3. Assioma di separazione

> Dato un insieme, possiamo formare il sottoinsieme dei suoi elementi che soddisfano una proprietà

$\forall X ,\exists Y ,\forall Z ,(Z \in Y \Leftrightarrow Z \in X \wedge P (Z ))$

per ogni X esiste un Y, tutti gli insiemi in Z sono elementi di Y se sono appartenenti a X e hanno la proprietà

Abuso di notazione: $X =\{Y \in U| Y \notin Y\}$

> Attenzione: per descrivere Y c'è un abuso di notazione $\{Z \in X |P(Z)\}$ (Z è un elemento)

### 4.2.4. Assioma dell’insieme vuoto

> L’insieme X viene indicato come $\emptyset$

$\exists X ,\forall Z ,Z \notin X$

### 4.2.5. Definizione dell’insieme vuoto

> L’assioma è ridondante. Sia Y un qualunque altro insieme di cui un assoma asserisce l’esistenza (vedi p.e. assioma dell’infinito)

$\emptyset \coloneqq \{X \in Y |false\}$

### 4.2.6. Definizione di intersezione binaria


$A \cap B \coloneqq \forall Z\{Z\in A |Z\in B\}$

**teorema**

$X \in A \cap B \Leftrightarrow X \in A \wedge X \in B$

### 4.2.7. Definizione di intersezione

metto tutti gli insiemi da intersecare in F.

$\bigcap F \coloneqq \{ X \in A | \forall Y (Y \in F \Rightarrow X/Right \in Y) \}, A \in F$

### 4.2.8. Assiome dell'unione binaria

$\forall A,\forall B,\exists X ,\forall Z ,(Z \in X \Leftrightarrow Z \in A \vee Z \in B)$

### 4.2.9. Assioma dell'unione 

$\forall F \exists X \forall Z (Z\in X \Leftrightarrow \exists Y (Y \in F \wedge Z \in Y))$

### 4.2.10. 4.2.10 Assioma del singoletto

$\forall X, \exists Y \forall Z (Z \in Y \Leftrightarrow Z = X)$

l'insieme Y viene indicato come {X}

> grazie a questo insieme possiamo creare un infinità di insiemi,
> possiamo creare infiniti insiemi partendo da $\emptyset$ divente $\{\emptyset\}$  e combinato con l'unione si possono unire questi insiemi 

**(Abuso di) notazione**
Con la notazione $\{A_1, . . . , A_n\}$ indicheremo l’insieme $\{A_1\} \cup . . . \cup \{A_n\}$ che esiste in virtu degli assiomi del singoletto è dell’unione.

$X \in \{A_1,...,A_n\}$ sse $X=A_1$ oppure ... oppure $X=A_n$ .

### 4.2.11. Assioma dell’infinito
Esiste un insieme che contiene almeno tutti (gli encoding de)i numeri naturali.

$\exists Y( \emptyset \in Y \wedge \forall N (N \in Y \Rightarrow N \cup \{N\} \in Y))$

Indichiamo temporaneamente con N tale insieme 



### 4.2.12. Teorema esistenza di $N$

combinaimo altri assiomi con quello dell'infinito si arriva a dimostrare l'esistenza dell'insmieme N  che contiene tutti e soli i numeri naturali.

### 4.2.13. Assioma dell'insieme potenza

Esiste l'insieme dei sottoinsiemi di un inseme dato.

$\forall \exists Y, \forall Z ( Z \in Y \Leftrightarrow Z \subseteq X$

per ogni insieme X esiste un Y tale per cui, ogni Z elemento di Y se e solo se Z è un sottoinsieme di X

abuso di notazioni:$2^x$ oppure $P(x)$

> es  
> $2^{\{1,2\}}= \{\emptyset, \{1\},\{2\},\{1,2\}\}$

### 4.2.14. Assioma di regolarita (non da studiare) 

Ogni insieme non vuoto ha un elemento dal quale e disgiunto (senza elementi in comune ).Fra le conseguenze: nessun insieme contiene (ricorsivamente) se stesso e ha quindi senso cercare di misurare la taglia (chiamata cardinalita) di un insieme.

$A=\{\emptyset , \{ \emptyset\}\}$

$\emptyset \in A$ 
$\emptyset \cup A = \emptyset$ 

a e l'insime vouto soon disgiunti

### 4.2.15. Assioma di rimpiazzamento

Intuitivamente: l’immagine di un insieme rispetto a una formula che descrive una funzione e ancora un insieme. Intuitivamente: se A e un insieme, quindi  e abbastanza piccolo, e a ogni elemento ne associo un altro, in una relazione molti-a-uno, quello che ottengo come immagine e ancora piccolo.



## 4.3. Costruzioni dei Numeri Naturali

Assumo di avere i numeri reali con la mia meta matematica e li codifico con i miei insiemi

$\llbracket 0 \rrbracket \coloneqq \emptyset$  
$\llbracket n+1 \rrbracket \coloneqq \llbracket n \rrbracket \cup \{\llbracket n \rrbracket \}$

> esempi
> $\llbracket 0 \rrbracket =\emptyset$
> $\llbracket 1 \rrbracket =\{\emptyset\}$
> $\llbracket 2 \rrbracket =\{\emptyset,\{\emptyset\}\}$
> $\llbracket 3 \rrbracket =\{\emptyset,\{\emptyset\}\,\{\emptyset,\{\emptyset\}\}\}$

# 5. Dimostrazioni


> regole di introduzione: sono quelle da utilizzare se voglio lavorare sulla conclusione, servono per introdurre una dimostrazione

> regole di eliminazione: servono per lavorare sull'ipotesi, la utilizziamo quando noi sappiamo già qualcosa

> postulato(o assioma):sono delle ipotesi che diamo per vere

> assioma: è un ipotesi che diamo per vera da quel momento in avanti

> enunciato di un teorema e ci  o che vogliamo dimostrare. Si compone di un insieme di ipotesi e di una conclusione


ogni passaggio va a lavorare su:
- le ipotesi
- la conclusione: che è quello che vogliamo andare a dimostrare in un determinato momento

## 5.1. Per Ogni $\forall$

**introduzione**:Per dimostrare $\forall x P(x)$ (per ogni x vale P(x))

> “sia x (un insieme) fissato; . . .”   
> (i “. . .” sono una prova di P(x))

**eliminazione**:Per ogni ipotesi o risultato intermedio $\forall x P(x)$ potete concludere che P valga ciò che volete

## 5.2. Implicazione $\Rightarrow$

**introduzione**: Per dimostrare $P \Rightarrow Q$

> “Assumo P (H). . . .”
> (“H”) e il nome dell’ipotesi; `
> i “. . .” sono una prova di Q)


**eliminazione**: Da un’ipotesi o un risultato intermedio $P \Rightarrow Q$ e da un’ipotesi o un risultato intermedio P potete concludere che Q vale.


**eliminazione** (variante): Da un’ipotesi o un risultato intermedio $P \Rightarrow Q$ di nome H , se volete concludere Q, potete procedere dicendo "per H , per dimostrare Q mi posso ridurre a dimostrare P" 


## 5.3. Coimplica $\Leftrightarrow$

**introduzione**: Per dimostrare $P \Leftrightarrow Q$ allora devo dimostrare $P \Rightarrow Q$ e $Q \Rightarrow Q$

**eliminazione**:L'ipotesi $P \Leftrightarrow Q$ può essere usata sia come ipotesi $P \Rightarrow Q$ che come $Q \Rightarrow P$

## 5.4. Espansione Definizioni

> **P ovvero Q**: serve per espandere P ottenendo la frase Q


## 5.5. Regola della eliminazione dimostrazione

Da un ipotesi o un risltato intermetdio $p \Rightarrow Q$ di nome H, se volete concludere Q potete dire

## 5.6. Regola dell'assurdo

Se attraverso le altre ipotesi rendono P falso, $P \Rightarrow assurdo$

## 5.7. Congiunzione

**introduzione**: per dimostrare $P \wedge Q$: P e Q , si dimostrano sia P che Q

**eliminazione**:per eliminazione, può essere usato sia P che Q. in alternativa invece di concludere o assumere $P \wedge Q$ si può direttamente concludere o assumere $P (H_1)$ e $Q (H_2)$.

## 5.8. Disginuzione

**introduzione**: per dimostrare $P \vee Q$ basta dimostrare P oppure Q dichiarandolo   
> "dimostro P" oppure "dimostro Q"

**eliminazione**:Data un’ipotesi o un risultato intermedio $P \vee Q$, si può proseguire nella dimostrazione per casi, una volta assumendo
che P valga e una volta che Q valga:
> “procedo per casi:  
> caso in cui valga P (H ): . . .  
> caso in cui valga Q (H ): . . . ”   


## 5.9. Risultati intermedi

Potete anche utilizzare una **regola di introduzione** per dimostrare un **nuovo risultato intermedio**, diverso dalla conclusione corrente, a cui date un nome per utilizzarlo in seguito, a patto che abbiate già a disposizione le **premesse** della regola

## 5.10. esiste

## 5.11. Abbreviazioni

- **per ogni tale che**:
> “sia x tale che P(x). . . .”
> abbrevia
> “sia x (un insieme) fissato; assumo P(x); . . . ”
> per dimostrare $∀x P(x) \Rightarrow Q(x)$

- **Da $H_1, . . . , H_n$**:
- **Quindi**:

# Relazioni, Funzioni ...

## Coppie ordinate

> negli insiemi l'ordine non conta e nemmeno la numerosità degli elementi

**coppie ordinate**: Una coppia ordinata, invece, e formata da due componenti di cui uno e identificato come primo e l’altro come secondo. Due  coppie sono uguali sse lo sono rispettivamente il primo e il secondo elemento

**Una coppia non è l'insieme dei suoi elementi e non deve essere pensata come contenete i suoi elementi**
Una coppia ordinata $\langle 1,2 \rangle$ si può rappresentare come un insieme scrivendo $\{X,\{X,Y\}\}$

### teorema di caratterizzazione delle coppie


$\langle X,Y \rangle = \langle X^1 Y^1 \rangle \Leftrightarrow X= X^1 \wedge Y=Y^1$

**crollario**:$\langle X, Y\rangle \neq \langle Y, X \rangle \text{a meno che} X=Y$

## Teorema del prodotto cartesiano tra gli insiemi

a partire da due insiemi A e B possiamo creare il **prodotto cartesiano** che viene indicato con l'abuso di notazione AxB.

$\forall A \forall B, \exists C,\forall Z,(Z\in C \Leftrightarrow \exists a,\exists b, ( a \in A \wedge b \in B \wedge Z=\langle a,b \rangle))$

**es**: $\{a,b\} \times \{1,2\}= \{\langle a,1\rangle,\langle a,2\rangle,\langle b,1 \rangle,\langle b,2\rangle\}$

## Relazione 

Una **relazione** fra A e B è un qualunque sottoinsieme di  $A \times B$.

**Elementi in relazione**  
Sia $\mathit{R}$ una relazione. Scriviamo $a\mathit{R}b \text{ sse  } \langle a,b\rangle \in \mathit{R}$

### Teorema: relazioni verso insiemi vuoiti

Se $\mathit{R} \subset A \times \emptyset$ oppure $\mathit{R} \subset  \emptyset \times  A$ allora $\mathit{R}$

Dimostrazione: non posso formare coppie prendo uno dei due elementi dall'insieme vuoti, perché tale insieme è vuoto.

<details>
  <summary>
  esempio 
  </summary>

la relazione $\le$ sull'insieme numerico $\{0,1,2\}$ è definita come segue:  
$\le \coloneqq \{\langle 0,0 \rangle ,\langle 0,1 \rangle ,\langle 0,2 \rangle ,\langle 1,1 \rangle ,\langle 1,2 \rangle,\langle 2,2 \rangle  \}$ e $0\le 2$ è una notazione per $\langle 0,2\rangle \in \le$

</details>

## Dimostrazione Di Funzioni

Una **funzione di dominio** A e codominio B e una qualunque relazione $f \subset A \times B$ tale che: $\forall X,(X \in A \Leftarrow \exists! Y , X f Y)$

per ogni elemento del dominio c'è un **unico** elemento del codominio

**Abuso di notazione**  
Sia f una funzione. Scriviamo  $y=f(x)$ per dire $xfy$,ovvero $\langle x,y \rangle \in f$

### Teorema esistenza dello spazio di funzioni come insieme

$\forall A, \forall B,\exists C,\forall f,(f \in C \Leftrightarrow f \text{ è una funzione di dominio  A e codominio B})$

Abuso di notazione $B^{A}$ (spazionio delle funzioni da A a B)

<details>
  <summary>
  es  
  </summary>

$\{1,2\}^{\{a,b\}} = \{\{\langle a,1\rangle,\langle b,1\rangle \},\{\langle a,1\rangle,\langle b,2\rangle \},\{\langle a,2\rangle,\langle b,1\rangle \},\{\langle a,2\rangle,\langle b,2\rangle \}$

</details>

**Spazio di funzioni verso insiemi vuoti**

$B^{\emptyset}=\emptyset$  
$\emptyset^A=\emptyset se A\neq \emptyset$

## Abbreviazioni 


1. $\forall X \in A,P(X)$ indica  $\forall X (X \in A \Rightarrow P(X))$
1. $\exists X \in A,P(X)$ indica  $\exists X (X \in A \wedge P(X))$
1. $\forall X,Y \in A,P(X,Y)$ indica  $\forall X in A ,\forall Y \in A,P(X,Y)$
1. $\exists X,Y \in A,P(X,Y)$ indica $\exists X \in A , \exists Y \in A,P(X,Y)$

## Priorprietà delle relazioni

Sia $\mathit{R} \subset A \times A $.La relazione $\mathit{R}$ gode della proprietà
- riflessiva se $\forall X \in A,X\mathit{R}X$
- simmetrica se $\forall X,Y \in A,(X\mathit{R}Y \Leftarrow Y\mathit{R}X)$
- transitiva se $\forall X,Y,Z \in A,(X\mathit{R}Y \wedge Y\mathit{R}Z \Leftarrow X\mathit{R}Z)$

**es**:
- = : gode di tutte le proprietà

TODO: aggiungere gli es


### Relazioni di ordinamento strette

Una relazione $\mathit{R} \subset A * A$ è di ordine stretto sse $\mathit{R}$ è trenaisitva e non riflessiva

### Relazioni di ordinamento lasche

Una relazione $\mathit{R} \subset A \times A$ è di ordine lasco sse $\mathit{R}$ è trenaisitva e  riflessiva

### Relazioni di equivalenza $\equiv$

Una relazione $\mathit{R} \subset A \times A$ è equivalente sse $\mathit{R}$ è riflessiva, transitiva e simmetrica


l'**equivalenza è diversa dall'uguaglianza** perché nell'uguaglianza viene usata per confrontare oggetti meno di dettagli non ritenuti rilevanti per quello che si deve fare

### Classi di equivalenza

TODO: add

### Insieme quoziente

sia $\equiv \subseteq A*A$ una relazione di equivalensa.L'**insieme quoziente** di A ripetto a $\equiv$ è definito come:
$A_{/\equiv}\coloneqq \{[x]_{\equiv} | x \in A\}$


### Costruzione di Z

### Costruzione dei razionali

Q=$\mathbb{Z}\times \mathbb{Z}^0$ dove $\mathbb{Z}^0=\mathbb{Z}\/{0}$

Costruisco una relazione di equivalenza tra le coppie in Z come: $\langle a_1,b_1\rangle \equiv \langle a_2,b_2 \rangle \coloneq a_1\times b_2 =b_1 \times a_2$

$\mathbb{Q}\coloneqq $Q_{\/\equiv} = \{...,[\langle 2,3\rangle],...,[\langle 4,2\rangle],...\}$

la classe di equivalenza $[\langle 2,3\rangle]={\langle 2,3\rangle,\langle 4,6\rangle,...}$

## iniettiva surrettiva biettività

$f \in B^{A}$

- indiettiva 
- surretti
- biettiva

TODO: to complete



## Cardinatlità

Avere la stessa cardinalità
Due insiemi A, B hanno la stessa cardinalità sse esiste una
biiezione fra A e B.
Avere la stessa cardinalita è una “relazione di equivalenza”, ma `
sulla classe di tutti gli insiemi.

### Teorema: esistenza dei numeri cardinali come insiemi

Si possono costruire i numeri cardinali senza utilizzare le classi di equivalenza, ma lavorando solo con gli insiemi. quindi ogni numero cardinale viene ottenuto come un insime.

# Insiemi infiniti

Un insieme si dice **finito** quando **non è infinito**.

<details>
  <summary>
osservazione del finito  
  </summary>

intuitivamente sappiamo che un insieme con 3 elementi e finito. `
Immaginate un albergo con 3 stanze singole tutte occupate.
Arriva un nuovo cliente. Puo l’albergatore con una qualche `
manovra accomodare tutti i clienti nell’hotel rispettando il fatto
che una singola puo essere occupata da un solo cliente?
</details>


# 7. Dimostrazioni matematiche



> **Teorema**: E’ una proposizione con la quale si vuole affermare che un enunciato sia vero. Solitamente si presenta nella forma A,B,C,D… -> T, dove A,B,C,D sono le ipotesi e T la tesi.



