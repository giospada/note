
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
- [6. Dimostrazioni matematiche](#6-dimostrazioni-matematiche)



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

$\forall X ,\exist Y ,\forall Z ,(Z \in Y \Leftrightarrow Z \in X \wedge P (Z ))$

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

$\bigcap F \coloneqq \{ X \in A | \forall Y (Y \in F \Rightarrow X \in Y) \}, A \in F$

### 4.2.8. Assiome dell'unione binaria

$\forall A,\forall B,\exists X ,\forall Z ,(Z \in X \Leftrightarrow Z \in A ∨Z \in B)$

### 4.2.9. Assioma dell'unione 

$\forall F \exists X \forall Z (Z\in X \Leftrightarrow \exists Y (Y \in F \wedge Z \in Y))$



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



# 6. Dimostrazioni matematiche



> **Teorema**: E’ una proposizione con la quale si vuole affermare che un enunciato sia vero. Solitamente si presenta nella forma A,B,C,D… -> T, dove A,B,C,D sono le ipotesi e T la tesi.



