# Logica di prim'ordine

> Logica di prim0ordine è molto utilizzata dai matematici

la **Logica proposizionale** è quella logica le cui connotazioni denotano tutte valori di verità, è molto limitata quando si si sposta su **oggetti infiniti** ( **non cattura i quantificatori **, dicono quanto sia esteso l'insieme degli oggetti che soddisfa un predicato)

## Quantificatori

- esiste  $\exists$
- per ogni $\forall$

I quantificatori sono **utilizzati sugli elementi** del dominio, **non** sono utilizzabili su **funzioni e predicati**

## Definizione della Sintassi

Oltre ai quantificatori definiamo:
- variabili: denotano un oggetto ignoto e variabile sul dominio (es x,y,z..)
- constanti: denotano un oggetto noto e fissato del dominio (es 1,0,$\pi$,...)
- simboli di funzione: applicati a connotazioni di oggetti del dominio denotano un oggetto del dominio (es +,*,il fratello di ...)
- simboli di predicato: applicati a connotazioni di oggetti del dominio denotano un valore di verità (es $<,le,=,...$)

![](vx_images/84383600816995.png)

Ultima logica in cui vale la competenza e in alcuni casi anche la compattenza



## Formalizzazione

i quantificatori che abbiamo utilizzato non riescono a catturare tutti i quantificatori

### Binder

i quantificatori sono cais particolari di binder

Un binder **lega** una variabile di uno scope.

dentro lo scope la variabile verrà sostituita con un valore.

<details>
<summary>
esempi
</summary>

$\forall x. P$, una volta che calcola per tutti gli x prende il minimo


</details>


shodowing: qunado una variabile non è più utilizzabile in uno scope perchè è stata dichiarata in uno scope più interno

1. **collegare** ongi occorrenza di una variabile legata con un binder


![](vx_images/4954654139474.png)






![](vx_images/5586110706997.png)		



## Semantica

> un mondo o interpretazione per la logica del primo ordine è una coppia (A,i) dove A è un insieme non vuoto di denotazioni per i termini e l è una funzioen di interpretazione che associa



