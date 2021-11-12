# 08 Logica


## Funzioni Matematiche e Informatiche

**Matematica**:
l'operazine $+$ è una funzione, qundi un sottonsineme del prodotto cartesiano.(es $+ =\{\langle \langle 0 ,0\rangle\,0 \rangle, \langle \langle 3, 7 \rangle, 10\rangle ...\}$)

**Informatica**
viene definita come una procedura di calcolo, partendo dai i numeri in base uno `N = O | S R`, possiamo definiral in 4 modi.
```haskell

O `+ m =m 
S n `+ m =S (n `+ m)
-- possiamo scriverla con la ricorsione sul secondo membro
n +' O =n
n +' S n  =S (n +' m)
-- un altro modo  è tenere un accomulatore
O ``+ m=m
S n ``+ m = n ``+ S m
-- l'opposto dell'ultima
n +`` O = n
n +`` S n = S n ``+ m
```

Essendo che in matematica tutte le funzioni di somma sono uguali, ci chiediamo se anche queste lo siano.
Lo risultato è lo stesso ma calcola in modo diverso quindi non sono la stessa funzione.

Per esmpio
```haskell
-- 1000 + 2 -> 1002

-- utilizzando la prima funzione abbiamo
-- 1000 `+ 2 -> S(999`+2)-> S(S(998`+2)) -> .... -> S(S( .... `+ 2)) ->1002

-- utilizzando la seconda invece

-- 1000 +` 2 -> S(1000+'1)-> S(S(998+`0)) ->1002
```

queste funzioni differiescono su quale input calcolano e ne deriva che hanno un tempo d'esecuzione diverso.

```haskell
-- utilizzando la terza
-- 1000 ``+ 2 -> 999 ``+ S 2 -> 998 ``+ S (S 2) -> ... -> 0 ``+ 1002 -> 1002

```

> Lo **Stack** è quello dove vengono allocate le variabili locali e le chiamate di funzione, mentre la **Heap** alloca tutti i dati di lunghezza dinamnica.

la prima funzione utilizza le cella dello stack mentre la seconda della heap.

**Queste funzioni sono uguali, e sono uguali a quella matematica?**

Per definzione bisogna avere il dominio e il codominio uguale con la stessa legge d'associzione.

### Dimostrazione  che +' è uguale a '+

> lemma1 : m = O +' m

procedo su induzione strutturale  su m per dimostrare m = O +' m

**caso O:**
    devo dimostare che O = O +' O
    ovvero  O= O
    ovvio


**caso S x:**
    per ipotesi induttiva $\forall x$ x = O +' x (H)
    devo dimostrare che $\forall x$ S x = O +' S x
    ovvero $\forall x$ S x = S (O +'  x )
    ovvio per H


> lemma2 : S (x +' m) = S x +' m

procedendo su induzione strutturale su m per dimostrare S( x +' m )= S x +'m 

**caso O:**
    debbo dimostrare $\forall x$ S(x +' O)= S x +' O
    ovvero $\forall x$ S (x )= Sx
    ovvio
    
**Caso S y:**
    per induzione abbiamo che $\forall x$ S (x +' y ) = S x +' y (H)
    dobbiamo dimostrare $\forall x$ S (x +' (S y))= S x +' S y
    ovvero $\forall x$ S (S (x +'  y))= S x +' S y
    ovvero  $\forall x$ S( S (x +' y))= S(S x +' y) 
    sias x un numero naturale
    ovvio per H


> Dim1: n '+ m = n +'  m

Procediamo per ricorsione strutturale su n  per dimostrare $\forall$ m. n '+m = n +' m

**Caso 0:**
    dimostro  $\forall m.$ O '+m= O +` m
    ovvero     $\forall$ m= 0 +' m
    ovvio per lemma1


**Caso S x:**
   per induzione strutturale $\forall$ m x '+ m = x +' m (H)
   devo dimostrarem $\forall$ m S x '+ m = S x +' m 
   ovvero  $\forall$m S (x '+ m)= S x +' m
   siam m un numero per ipotesi H possiamo riscrivere
   S ( x +' m) = S x +' m
   ovvio per lemma2


### Altre prove


`nth  n l ` ( restutiusce  l'n-esimo elemento di l se l è sufficentemente lunga)


la definisco per ricorsione strutturale su n:
- tutte le prduzioni di n una e una sola volta
- le chiamate ricorsive solamente su sottoformule immedite dell'input n


`head []=6699 --possiamo far restituire qualsiasi cosa`
`head (n:l)=n`

`tail []=6699 -- possiamo fare restituire qualsiasi cosa `
`tail (n:l)=l`

`nth O l = head l` 
`nth (S n) l = nth n (tail l)` 

`nth 0 [] = 6699`
`nth (S n) [] =  6699`
`nth 0 (n:l) = n`
`nth (S n) (n:l) = nth n l` 

> therorema:
> ($\forall$ n. n < |l1| $\implies$ nth n l1 = nth n ( l1@ l2)) $\vee$
>  ($\forall$n. n  < |l2" $\implies$ nth n l2 = nth (|l1|+n)  (l1@l2)  )


case []:
$\displaylines{&}$ $\forall$l2. ($\forall$ n. n < |[]| $\implies$ nth n [] = nth n ( []@ l2)) $\vee$
$\displaylines{&}$ ($\forall$n. n  < |l2" $\implies$ nth n l2 = nth (|[]|+n)  ([]@l2)  )
$\displaylines{&}$ ovvero  
$\displaylines{&}\forall$l2. ($\forall$ n. n < 0 $\implies$ nth n [] = nth n ( []@ l2)) $\vee$
$\displaylines{&}$($\forall$n. n  < |l2" $\implies$ nth n l2 = nth (n)  (l2)  )
$\displaylines{&}$ dimostro $\forall$ n < 0 $\implies$ ...
 $\displaylines{&}$ sia n un numero t.c n < 0 
$\displaylines{&}$ assurdo.
$\displaylines{&}$ dimostr $\forall$n . n < |l2| $\implies$ nth n l2 = nth n l2
        ovvio
        