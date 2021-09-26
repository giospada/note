# Logica


## Introduzione 22/03/2021


![foto del professore con la giaguaro](img/proftigre.png)

> Claudio Sacerdoti Coen

### Logica

viene studiata da più discipline (fisica, matematica,informatica)

Domande chiave:
- cos'è la correttezza di un ragionamento?(e scriverlo in modo algoritmico)
- quali ragionamenti sono corretti?
- ci sono fatti non deducibili tramite un ragionamento?

la logica non parla di verità (più ragionamenti corretti)


## Paradossi (24/09/2021)

> Antinomia: è una conclusione inaccettabile,che deriva da premesse accettabili per mezzo di un ragionamento accettabile 

> Paradosso : conclusione contraria all'intuizione che deriva da premesse accettabili per mezzo di un ragionamento accettato (è accettabile)

<details>
<summary>
falso paradosso
</summary>

$x=1$
$x^2=x$
$x^2-1=x-1$
$(x-1)(x+1)=x-1$
$x+1=1$
$x=0$
</details>


### Linguaggio naturale

è alla base della comunicazione e del ragionamento umano

il linguaggio deve essere espressivo e viene esteso e specializzato (per comunicare )

Non possiamo utilizzarlo per procedure di calcolo e dimostrazioni perchè:
- Ambigui
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

Il linguaggio naturale ammette paradossi


<details>

es.1

"io mento"  

io mento se e solamente se cio che dico non ` e vero `  

io mento se e solamente se “io mento” non e vero `  

**io mento se e solamente se io non mento**

es.2

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

### Linguaggio matematico

è che rientrino i paradossi

nel 1900 la matematica viene ristrutturata dalle basi, con la teoria degli insiemi

la teoria degli insiemi parte dal presupposto che tutto è un insieme

Russell trova un paradosso su queste teorie

essendo che tutto è un insieme si può utilizzare il simbolo di appartenenza tra oggetti

questo operazione di esistenza fa crea un paradosso perché mi posso chiedere se un insieme contiene se stesso


<details>

$X =\{ Y| Y \notin  Y\}$

se x è un insieme che contiene tutti gli insiemi che non contengono se stessi

$X \in X \text{ sse } X \notin X$

- con  non può contenere se stesso per definizione, quindi $X \notin  X$
- 

</details>


per ovviare al paradosso:
- non è possibile formare liberamnete un insieme per una proprietà 
- ma è possibile selezionare elementi da un insieme esistente 
- la collezione di tutti gli insiemi non è un insieme

### I paradossi in informatica

nella programmazione ogni linguaggio può eseguire delle funzioni che possono prendono in input e danno in output altre funzioni


supponiamo che le funzioni scrivibili in un linguaggio di prograzione dato un input, restituiscano un output in tempo finito

Sia `f(g) = not (g(g))`

allora `f(f)= not (f(f))`

pertanto:
- O f non è scrivibile in P è altamente inespressivo
- Oppure f non è totale (diverge, cioè non mi da nessun output in un tempo finito)

Quindi le funzioni dei linguaggi di programmazione non sono funzioni matematiche




<details>

</details>

