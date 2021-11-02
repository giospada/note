

# Funzioni Esponenziali e Trigonometriche

## Funzione Esponenziale

definizione di esponenziale:  
$a \in \mathbb{R} , a<0 , a \neq 1$  
$y=a^x$
**oss**: $a>0$

<details>
<summary>
esempio
</summary>

$a=-2$

$(a)^3=-8$
$(a)^{\frac{6}{2}}\sqrt{-2^6}=\sqrt{64}=8$

non coincidono 
</details>


**Notazione**:

$\exp_a(x){:=} a^n$

(se si sceglie come base di a della funzione esponenziale il numero $e$, $e^x$ l'esponenziale a base naturale (nome per indicare la $e$))

$\exp : \mathbb{R} \rightarrow \mathbb{R}^{*}$


![esponenziale](vx_images/5303331546703.png )
![esponenzie](vx_images/3346331093181.png )

## Funzione Logaritmica

$a \in \mathbb{R} , a<0 , a \neq 1$  
$\forall y \in \mathbb{R}: y>0 \exists! x \in \mathbb{R}:$

$a^x=y$

$\log_a y {:=} x$ (si legge logaritmo di y in base a)

$\log : \mathbb{R}^{*}_{+} \rightarrow \mathbb{R}$


<details>
    <summary>
    esempi
    </summary>

$\log_2 16=4$  
$\log_2 1=0$
$\log_2 0=\text{non esiste}$
$3^{log_3 4}=4$
</details>

TODO: dimostrare che la funzine è inversa

![logaritmo](vx_images/4993496907525.png )

![](vx_images/3945607777711.png )

## Funzioni gognometriche

**circonferenza gognometrica**: circonferenza di raggio uno con il centro sugli assi $x^2+y^2=1$ (lunghezza $2\pi$)

TODO: add immagini
![](vx_images/2133540871851.png)

### Radianti

$\alpha°$: angolo in gradi (non da informazioni sulla lunghezza dell'angolo)  
$\alpha_r$: angolo in gradi

$\alpha°:360=\alpha_r:2\pi \\ \alpha_r=\frac{\alpha° \times \pi}{360}$  

### Seno e Coseno


sia $P(x_p,y_p)$ un punto sulla circonferenza goniometrica


![](../img/circonferenza_trigonometrica.png )

$\sin \alpha =y_p$  
$\cos \alpha =x_p$  

**Oss**: possiamo scrivere $\sin^2 \alpha +\cos^2\alpha=1$



$\sin \alpha =\sin \alpha \times 2\pi n$ dove $n \in \mathbb{N}$

si possono ricavare il $\sin$ dal $\cos$ e viceversa utilizzando la circonferenza goniometrica

$\sin \alpha=\mp \sqrt{1-\cos^2 \alpha}$


**Oss**:  
la funzione $\sin$ è dispari ($-\sin(\alpha)=\sin(-\alpha)$)

la funzione $\cos$ è pari ($\cos(\alpha)=\cos(-\alpha)$)

## Funzione Tangente

![](../img/tangente.png)

$\tan \alpha {:=} y_T$ (si legge tangente di  $\alpha$)

si come conseguenza della definizione si ha che :$\frac{\sin \alpha}{\cos \alpha}$

la tangente non è definita per:
- $\alpha = \frac{\pi}{2},\frac{3\pi}{2}..$
- $\alpha = -\frac{\pi}{2},-\frac{3\pi}{2}..$


## Angoli speciali

$\alpha= \frac{\pi}{4}$ è un angolo speciale perchè crea un triangono isocele.
![](vx_images/5116113239298.png)

così sappiamo che OA e PA sono uguali e ci basta risolvere $PO=\sqrt{OA^2+PA^2} \to PO^2=2PA^2 \to 1=2PA^2 \to PA= \frac{1}{ \sqrt{2}}$

quindi per quest'angolo ha:
$\sin \frac{\pi}{4}=\cos \frac{\pi}{4}=\frac{\sqrt{2}}{2}$
$tan \frac{\pi}{4}=1$


$\alpha= \frac{\pi}{4}$ è un angolo speciale perchè è di 30°.
![](vx_images/944801796821.png)

possiamo trasformarlo in questo modo ricavando un triangolo equilatero, e ricaviamo.

$\cos \frac{\pi}{6}=\frac{\sqrt{3}}{2}$
$\sin \frac{\pi}{6}=\frac{1}{2}$
$\tan \frac{\pi}{6}=\frac{\sqrt{3}}{3}$


## Grafici 

![](../img/grafsen.png)
![](../img/grafcos.png )
![](../img/graftan.png )

## Formule di Addizione e Sottrazione


$\cos(\alpha-\beta)=\cos \alpha \times \cos \beta +\sin \alpha \times \sin \beta$
 
$\cos(\alpha+\beta)=\cos \alpha \times \cos \beta -\sin \alpha \times \sin \beta$


$\sin(\alpha-\beta)=\sin \alpha \times \cos \beta -\cos \alpha \times \sin \beta$

$\sin(\alpha+\beta)=\sin \alpha \times \cos \beta -\cos \alpha \times \sin \beta$

$\cos (\frac{\pi}{2}-\alpha) =\sin \alpha$

$\sin (\frac{\pi}{2}-\alpha) =\cos \alpha$

**Dalle formule di addizione si ha**:
$\cos 2\alpha=\cos^2 \alpha -\sin^2 \alpha$
$\sin 2\alpha=2\sin \alpha \times \cos \alpha$

## Funzioni Gognometriche Inverse

### Arcsin

La funzione $\sin : \mathbb{R}\rightarrow \mathbb{R}$ non è inverstibile perchè non è suriettiva ne iniettiva.
Possiamo però restrigere il suo codominio a $\sin \mathbb{R}\rightarrow [-1,1]$  per farla diventare surrettiva;
Similmente renderla iniettiva modifichiamo il suo domninio a $\sin : [-\frac{\pi}{2},\frac{\pi}{2}]\rightarrow \mathbb{R}$,
così possiamo creare il seno biettivo come $\sin : [-\frac{\pi}{2},\frac{\pi}{2}]\rightarrow [-1,1]$.


La funzione inversa andrà $\arcsin : [-1,1] \rightarrow [-\frac{\pi}{2},\frac{\pi}{2}]$.

Quindi $\forall x \in [-\frac{\pi}{2},\frac{\pi}{2}] \\ \arcsin(\sin x)=x$ e 
quindi $\forall y \in [-1,1] \\ \sin(\arcsin y)=y$

![](vx_images/686515595913.png )

### Arccos

Similmente a come abbiamo visto per seno per creare l'inverso dell coseno dobbiamo renderlo binuivoco.
Per renderlo inietiva riduciamo il suo dominio a $[0,\pi]$ e per renderlo surrettivo definiamo il suo codominio $[-\frac{\pi}{2},\frac{\pi}{2}]$

Quindi $\forall x \in [-\frac{\pi}{2},\frac{\pi}{2}] \\ \arccos(\cos x)=x$ e 
quindi $\forall y \in [0,\pi] \\ \cos(\arccos y)=y$


![](vx_images/4969738921664.png)

### Arctan


Per renderlo inietiva riduciamo il suo dominio a $[-\frac{\pi}{2},\frac{\pi}{2}]$.


Quindi $\forall x \in ]-\frac{\pi}{2},\frac{\pi}{2}[ \\ \arccos(\cos x)=x$ e 
quindi $\forall y \in \mathbb{R} \\ \cos(\arccos y)=y$


![](vx_images/2312203870068.png ) 
