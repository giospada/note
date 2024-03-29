


# Dimostrazioni


> **Teorema**: E’ una proposizione con la quale si vuole affermare che un enunciato sia vero. Solitamente si presenta nella forma A,B,C,D… -> T, dove A,B,C,D sono le ipotesi e T la tesi.


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

## Implicazione $\implies$

**introduzione**: Per dimostrare $P \implies Q$

> “Assumo P (H). . . .”
> (“H”) e il nome dell’ipotesi; `
> i “. . .” sono una prova di Q)


**eliminazione**: Da un’ipotesi o un risultato intermedio $P \implies Q$ e da un’ipotesi o un risultato intermedio P potete concludere che Q vale.


**eliminazione** (variante): Da un’ipotesi o un risultato intermedio $P \implies Q$ di nome H , se volete concludere Q, potete procedere dicendo "per H , per dimostrare Q mi posso ridurre a dimostrare P" 


## Coimplica $\iff$

**introduzione**: Per dimostrare $P \iff Q$ allora devo dimostrare $P \implies Q$ e $Q \implies Q$

**eliminazione**:L'ipotesi $P \iff Q$ può essere usata sia come ipotesi $P \implies Q$ che come $Q \implies P$

## Espansione Definizioni

> **P ovvero Q**: serve per espandere P ottenendo la frase Q



## Regola dell'assurdo

[dimostrazione per assurdo](https://www.mathone.it/dimostrazione-per-assurdo/)

Se attraverso le altre ipotesi rendono P falso, $P \implies assurdo$

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

## Esiste


**introduzione**:
Per dimostrare $\exists x.P(x)$ (esiste un x per cui vale P(x)):
> “scelgo E e dimostro P(E) ; . . .”  
(i “. . .” è una prova di P(E))
E puo essere un’ ` espressione qualsiasi (es. B $\cap$ C).

**eliminazione**:
Da un’ipotesi o un risultato intermedio $\exists x.P(x)$ potete
procedere nella prova dicendo
> “sia x t.c. P(x) (H)”
x deve essere una variabile non in uso in nessuna ipotesi o nella conclusione

## Abbreviazioni

- **per ogni tale che**:
> “sia x tale che P(x). . . .”
> abbrevia
> “sia x (un insieme) fissato; assumo P(x); . . . ”
> per dimostrare $∀x P(x) \implies Q(x)$

- **Da $H_1, . . . , H_n$**:
- **Quindi**:
