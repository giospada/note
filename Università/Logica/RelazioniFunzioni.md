
# 3. Relazioni, Funzioni ...

## 3.1. Coppie ordinate

> negli insiemi l'ordine non conta e nemmeno la numerosità degli elementi

**coppie ordinate**: Una coppia ordinata, invece, e formata da due componenti di cui uno e identificato come primo e l’altro come secondo. Due  coppie sono uguali sse lo sono rispettivamente il primo e il secondo elemento

**Una coppia non è l'insieme dei suoi elementi e non deve essere pensata come contenete i suoi elementi**
Una coppia ordinata $\langle 1,2 \rangle$ si può rappresentare come un insieme scrivendo $\{X,\{X,Y\}\}$

### 3.1.1. teorema di caratterizzazione delle coppie


$\langle X,Y \rangle = \langle X^1 Y^1 \rangle \Leftrightarrow X= X^1 \wedge Y=Y^1$

**crollario**:$\langle X, Y\rangle \neq \langle Y, X \rangle \text{a meno che} X=Y$

## 3.2. Teorema del prodotto cartesiano tra gli insiemi

a partire da due insiemi A e B possiamo creare il **prodotto cartesiano** che viene indicato con l'abuso di notazione AxB.

$\forall A \forall B, \exists C,\forall Z,(Z\in C \Leftrightarrow \exists a,\exists b, ( a \in A \wedge b \in B \wedge Z=\langle a,b \rangle))$

**es**: $\{a,b\} \times \{1,2\}= \{\langle a,1\rangle,\langle a,2\rangle,\langle b,1 \rangle,\langle b,2\rangle\}$

## 3.3. Relazione 

Una **relazione** fra A e B è un qualunque sottoinsieme di  $A \times B$.

**Elementi in relazione**  
Sia $\mathit{R}$ una relazione. Scriviamo $a\mathit{R}b \text{ sse  } \langle a,b\rangle \in \mathit{R}$

### 3.3.1. Teorema: relazioni verso insiemi vuoiti

Se $\mathit{R} \subset A \times \emptyset$ oppure $\mathit{R} \subset  \emptyset \times  A$ allora $\mathit{R}$

Dimostrazione: non posso formare coppie prendo uno dei due elementi dall'insieme vuoti, perché tale insieme è vuoto.

<details>
  <summary>
  esempio 
  </summary>

la relazione $\le$ sull'insieme numerico $\{0,1,2\}$ è definita come segue:  
$\le \coloneqq \{\langle 0,0 \rangle ,\langle 0,1 \rangle ,\langle 0,2 \rangle ,\langle 1,1 \rangle ,\langle 1,2 \rangle,\langle 2,2 \rangle  \}$ e $0\le 2$ è una notazione per $\langle 0,2\rangle \in \le$

</details>

## 3.4. Dimostrazione Di Funzioni

Una **funzione di dominio** A e codominio B e una qualunque relazione $f \subset A \times B$ tale che: $\forall X,(X \in A \Leftarrow \exists! Y , X f Y)$

per ogni elemento del dominio c'è un **unico** elemento del codominio

**Abuso di notazione**  
Sia f una funzione. Scriviamo  $y=f(x)$ per dire $xfy$,ovvero $\langle x,y \rangle \in f$

### 3.4.1. Teorema esistenza dello spazio di funzioni come insieme

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

## 3.5. Abbreviazioni 


1. $\forall X \in A,P(X)$ indica  $\forall X (X \in A \Rightarrow P(X))$
1. $\exists X \in A,P(X)$ indica  $\exists X (X \in A \wedge P(X))$
1. $\forall X,Y \in A,P(X,Y)$ indica  $\forall X in A ,\forall Y \in A,P(X,Y)$
1. $\exists X,Y \in A,P(X,Y)$ indica $\exists X \in A , \exists Y \in A,P(X,Y)$

## 3.6. Priorprietà delle relazioni

Sia $\mathit{R} \subset A \times A $.La relazione $\mathit{R}$ gode della proprietà
- riflessiva se $\forall X \in A,X\mathit{R}X$
- simmetrica se $\forall X,Y \in A,(X\mathit{R}Y \Leftarrow Y\mathit{R}X)$
- transitiva se $\forall X,Y,Z \in A,(X\mathit{R}Y \wedge Y\mathit{R}Z \Leftarrow X\mathit{R}Z)$

**es**:
- = : gode di tutte le proprietà

TODO: aggiungere gli es


### 3.6.1. Relazioni di ordinamento strette

Una relazione $\mathit{R} \subset A * A$ è di ordine stretto sse $\mathit{R}$ è trenaisitva e non riflessiva

### 3.6.2. Relazioni di ordinamento lasche

Una relazione $\mathit{R} \subset A \times A$ è di ordine lasco sse $\mathit{R}$ è trenaisitva e  riflessiva

### 3.6.3. Relazioni di equivalenza $\equiv$

Una relazione $\mathit{R} \subset A \times A$ è equivalente sse $\mathit{R}$ è riflessiva, transitiva e simmetrica


l'**equivalenza è diversa dall'uguaglianza** perché nell'uguaglianza viene usata per confrontare oggetti meno di dettagli non ritenuti rilevanti per quello che si deve fare

### 3.6.4. Classi di equivalenza

TODO: add

### 3.6.5. Insieme quoziente

sia $\equiv \subseteq A*A$ una relazione di equivalensa.L'**insieme quoziente** di A ripetto a $\equiv$ è definito come:
$A_{/\equiv}\coloneqq \{[x]_{\equiv} | x \in A\}$


### 3.6.6. Costruzione di Z

### 3.6.7. Costruzione dei razionali

Q=$\mathbb{Z}\times \mathbb{Z}^0$ dove $\mathbb{Z}^0=\mathbb{Z}\/{0}$

Costruisco una relazione di equivalenza tra le coppie in Z come: $\langle a_1,b_1\rangle \equiv \langle a_2,b_2 \rangle \coloneq a_1\times b_2 =b_1 \times a_2$

$\mathbb{Q}\coloneqq $Q_{\/\equiv} = \{...,[\langle 2,3\rangle],...,[\langle 4,2\rangle],...\}$

la classe di equivalenza $[\langle 2,3\rangle]={\langle 2,3\rangle,\langle 4,6\rangle,...}$

## 3.7. iniettiva surrettiva biettività

$f \in B^{A}$

- indiettiva 
- surretti
- biettiva

TODO: to complete



## 3.8. Cardinatlità

Avere la stessa cardinalità
Due insiemi A, B hanno la stessa cardinalità sse esiste una
biiezione fra A e B.
Avere la stessa cardinalita è una “relazione di equivalenza”, ma `
sulla classe di tutti gli insiemi.

### 3.8.1. Teorema: esistenza dei numeri cardinali come insiemi

Si possono costruire i numeri cardinali senza utilizzare le classi di equivalenza, ma lavorando solo con gli insiemi. quindi ogni numero cardinale viene ottenuto come un insime.

## 4. Insiemi infiniti

Un insieme si dice **finito** quando **non è infinito**.

<details>
  <summary>
osservazione del finito  
  </summary>

intuitivamente sappiamo che un insieme con 3 elementi e finito. `
Immaginate un albergo con 3 stanze singole tutte occupate.
Arriva un nuovo cliente. Puo l’albergatore con una qualche
manovra accomodare tutti i clienti nell’hotel rispettando il fatto
che una singola puo essere occupata da un solo cliente?
</details>

<details>
  <summary>
Infinito con l  Metafora dell'albego di Hilbert
  </summary>

Intuitivamente sappiamo che l’insieme dei numeri naturali e infinito. `
Immaginate un albergo con una stanza singola per ogni numero
naturale, tutte occupate. Arriva un nuovo cliente. Puo l’albergatore `
con una qualche manovra accomodare tutti i clienti nell’hotel
rispettando il fatto che una singola puo essere occupata da un solo `
cliente?
</details>

Un insieme A si dice **infinito** quando è in biderezione con un suo sottoinsieme proprio $B$ i.e $B \subsetneq \text{ e } |A|=|B|$

TODO: add birezione

### 4.1. $\le$ su numeri cardinali

TODO: aggiungere
