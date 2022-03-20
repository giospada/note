# Primitiva

**Definizione** $f : ]a,b[ \to \mathbb{R}$, prendiamo una funzione $F$ si dice primitiva (se è derivabile nell'intervallo) $f \text{ su } ]a,b[$ se vale $F'(x)=f(x)$

<details>
<summary>
esempio
</summary>

es : $f(x)=x, x \in \mathbb{R} F(x)=\frac{x^2}{2}$ è una primitiva $f$ su $\mathbb{R} (D \frac{x^2}{2}=x , \forall x)$  e ne posso trovare infinite aggiungendo delle costanti $G(x)=\frac{x^2}{2}+k$ è primitiva di $f \space  \forall k \in \mathbb{R}$ 
</details>


## Osservazioni 

**Oss:** una **funzione ha infinite primitive** perchè si può aggiungere una costante che poi viene persa quando si fa la derivata

**Prop:** sia $f: ]a,b[ \to \mathbb{R}$  siano $F,G :]a,b[ \to \mathbb{R}$ due primitive di f piccolo su $]a,b[$ Allora $\forall x \in ]a,b[, \exists k \in \mathbb{R}, F(x) - G(x) =k$ 

<details>
<summary>
esempio
</summary>

es $f(x)=\frac{1}{x^2} , x\neq 0, x \in \mathbb{R} \backslash \{0\}$ $F(x)=-\frac{1}{x}$ primitiva di $f$ su $\mathbb{R} \backslash \{0\} G(x)=\begin{cases}-\frac{1}{x}  & \text{ se } x> 0 \\ -\frac{1}{x}+2 & \text{ se } x <0 \end{cases}$ allora  $F'(x)=G'(x)=\frac{1}{x^2} \text{ma } G(x)-F(x)=\begin{cases}0  \text{ se } x> 0 \\ 2 \text{ se }  x <0 \end{cases}$ 
</details>



**Dim** considero $H: ]a,b[ \to \mathbb{R} ,\space H(x)=F(x)-G(x) ,$ $\space H'(x)=F'(x)-G'(x)=f(x)-f(x)=0,$ $\forall x \in ]a,b[ \space \exists k \in \mathbb{R} , H(x)=k$  


# Funzione integrale

> la funzione integrale è una funzione che parte da un punto e calcola l'area fino ad un altro punto preso come variabilie

**Def :** sia $f : ]a_0,b_0[ \to \mathbb{R}$ sia $c \in ]a_0,b_0[$ definisco $I_c : ]a_0,b_0[ \to \mathbb{R}, I_c(x)=\int_c^x f(t) dt = \int_c^x f$  

## Proprietà
**osservazione** $I_c (c)= \int^c_c f = 0$

 **osservazione** siano $c_1,c_2 \in ]a_0,b_0[ ,\space  f$ continua $I_{c_1}(x)=\int_{c_1}^x f , I_{c_2}(x)=\int_{c_2}^x f$ , $I_{c_1}(x)- I_{c_2}(x)=\int_{c_1}^x f - \int_{c_2}^x f= \int_{c_1}^x f + \int^{c_2}_x f = \text{proprieta add}= \int_{c_1}^{c_2} f(t) dt$  dunque $I_{c_1}(x) I_{c_2}$ differeiscono per una constante



## Teorema Fondamentale del Calcolo Integrale

$f: ]a,b[ \to  \mathbb{R}\space$ continua $, c \in ]a,b[$ $\forall x \in ]a,b[$, $I_c$ è derivabilie in x  e vale  $I'_c(x)=f(x)$

$(\frac{d}{dx} \int_c^x f(t) \space dt =f(x) \forall x \in ]a,b[)$

<details>
<summary>
esempio
</summary>
   
$F(x)= \int_0^x log(1+t^2)e^{-\sqrt{1+t^4}} dt$

possiamo semplicemente calcolare la derivata di f prendendo la funzione dentro l'integrale

$F'(t)=  log(1+t^2)e^{-\sqrt{1+t^4}}$


</details>

### Dimostrazione

$f:]a,b[\to \mathbb{R} \space I'_c(x)=f(x) \iff \displaystyle \lim_{h \rightarrow 0} \frac{I_c(x+h)-I_c(x)}{h}=f(x)$

caso $h \to 0+$:

$I_c(x+h) - I_c(x)=\int_c^{x+h}f -\int_c^xf=\int_c^{x+h}f +\int_x^cf=\int_x^{x+h} f$


$\displaystyle \lim_{h \rightarrow +0} \frac{1}{h}\int_x^{x+h} f = f(x) \iff \forall h_n \to 0+, \displaystyle \lim_{x \rightarrow +\infty} \frac{1}{h_n} \int_x^{x+hn} f= f(x)$  posso applicare il teorema della media integrale $\exists c_n \in ]x,x+h_n[ \text{ tale che } \frac{1}{h_n} \int_x^{x+hn}=f(c_n) \text{ con n che tende a più infinito e con f continua tende a } f(x)$

## Teorema fondamentale del calcolo (Formula di torricelli)

**Teorema:** Sia $f:]a_0,b_0[ \to \mathbb{R}$ continua, Sia $F:]a_0,b_0[ \to \mathbb{R}$ primitiva di $F$ e siano $a,b \in ]a_0,b_0[$  allora vale $\int _a^b f(x) \space dx =F(b)-F(a)=[F(x)]_a^b=F(x)|_a^b$


<details>
<summary>
esempio
</summary>

fai un esempio del calcolo.

</details>


Dim : Per il teorema (versione 1), fissata $c\in ]a,b[$ $I_c$ è una proimitiva di $f$. F è una primitiva di $f \implies \exists k\in \mathbb{R}$ tale che $F(x) = I_c(x)+k \forall x \in ]a,b[, \space F(b)-F(a)=I_c(b)+k-(I_c(a)+k)$ $=I_c(b)-I_c(a)=\int_c^b f - \int_c^a f$ $= \int_c^b f + \int _a^c f=\int_a^b f(x)\space dx$ 



# Tabella primitive

|               f                |                                                                 F                                                                  |
| ----------------------- | ----------------------------------------------------------------------------------------------------- |
| $x^n$                     | $\frac{x^{n+1}}{n+1}$  $n \in \mathbb{N} \backslash \{0\}, x\in \mathbb{R}$            |
| $x^k$                     | $\frac{x^{k+1}}{k+1}$  con $k \in \mathbb{Z}\wedge k \neq -1, x\neq 0$                    |
| $\frac{1}{x}$          | $ln(\|x\|)$  con $x\neq 0$                                                                                             |
| $x^{\alpha}$           | $\frac{x^{\alpha +1}}{\alpha +1}$  con $\alpha \in \mathbb{R}\backslash \{-1\},x>0$ |
| $cos(x)$                  | $sin(x)$                                                                                                                        |
| $sin(x)$                   | $-cos(x)$                                                                                                                      |
| $e^x$                     | $e^x$                                                                                                                          |
| $\frac{1}{1+x^2}$  | $\arctan(x)$                                                                                                                 |
| $\frac{1}{cos^2x}$ | $\tan(x)$                                                                                                                      |
| $\ln x$                     | $x \ln x - x$                                                                                                                  |


## Primitive di funzioni composte

**primitiva generale di funzioni composte** $f:I\to J, g: J \to \mathbb{R}, I, J$ intervalli aperti, $f,g$ derivabile, allora $g \cdot f$ è derivabile in I $(g \cdot f)(x)=g(f(x))$ vale 
$(g \cdot f) (x)=g'(f(x))- f'(x) \forall x \in I, g \cdot f$ è una primitiva di $h(x)=g'(f(x))f'(x)$ $\implies \int_a^b g'(f(x))f'(x) dx$ $=[g(f(x))]^{x=b}_{x=a}$

**Altre derivate composte**
1. $g(z)=e^z, g'(z)=e^z,$ $\space \int e^{f(x)}f'(x) \space dx=[e^{f(x)}]^{x=b}_{x=a}$
2. $g(z) = ln(z), g'(x)=\frac{1}{z} z>0$ $\space \int_a^b \frac{f'(x)}{f(x)} dx = [ln f(x)]_{x=a}^{x=a}$  
3. $g(z) = sin(z), g'(x)=cos(z),$  $\space \int_a^b cos(f(x))f'(x) dx = [sin(f(x))]_{x=a}^{x=a}$  
4. $g(z) = \frac{z^\alpha}{\alpha +1 }, g'(x)=z^{\alpha}, \alpha\neq -1, z \in$  dominio della potenza di $\alpha+1 \space \int_a^b f(x)^{\alpha}f'(x) dx = [\frac{f(x)^{\alpha+1}}{\alpha+1}]_{x=a}^{x=a}$  



**esponenziale**
$\int a^x \space dx=\int e^{x\ln a} \space dx= \frac{1}{\ln a} \int \ln{a} \space  e^{x \ln a}=[\frac{1}{\ln a}e^{x \ln a}]=\frac{1}{\ln a } a^x$


# Formula di integrazione per parti

$I \subseteq \mathbb{R},f$ dove è una funzione continua su $I, g$ derivabile su $I,g'$ continua, $F$   primitiva di $f$ su $I$  
$F$, $F(x)g(x)=F'(x)g(x)+F(x)g'(x), \forall x \in I$


Sia $[a,b]\subseteq I, \int_a^b \frac{x}{dx}F(x)g(x) dx=\int_a^b fg + \int_a^b Fg'=[F(x)g(x)]^b_a$ 

quindi
$\int_a^b f(x) g(x) \space  dx=[F(x)g(x)]_a^b - \int F(x)g'(x) dx$


<details>
<summary>
dim
</summary>

$I \subseteq \mathbb{R}$  intervallo  aperto $c\in I, I_c(x)=\int_c^x f(t) \space dt$ (f continua ) $TDC:I_c'(x)=f(x), \frac{d}{dx} \int_c^x f(t) dt=f(x)$

Se considero $H(x) = \in_x^c f(t) \space dt, H'(x)=\frac{d}{dx}( - \int_c^x f(t)\space dt \bigr)=-f(x)$

$\frac{d}{dx} \int_x^{x^3} f(t) \space dt$ sia $f \cdot I \to \mathbb{R}$ continua $h: \mathbb{R} \to I$ vogliamo allora $- \frac{d}{dx} \int_c^{h(x)} f(t) \space dt$  dove h deve essere una funzione derivabile


Scrivo $I_c(z)= \int_c^z f(t) \space dt ,\forall z \in I$ 

Scrive $\int_c^{h(x)}f(t) \space dt=I_c h(x)=I_c \cdot h(x)$ 


se h è derivabile f è continua, la funzione $I_c$ è derivabile (Teorema Fondamentale Calcolo). Dunque $(I_c \cdot h)'(x)=I_c(h(x))*h'(x)$ (derivata f. compota) $= f(h(x)) h'(x)$
</details>

## Generalizzazione Teorema Fondamentale del Calcolo

$f:I \to \mathbb{R}$ continua.
$g:\mathbb{R} \to I$ derivabile

allora vale:

$\frac{d}{dx}=\int_c^{h(x)} f(t) dt = f(h(x)) h'(x)$

# Cambio di Variabile

Cambio di variabile $x=h(t)$ in $\int f(x) dx$.

**Teorema**: $I,J\subset \mathbb{R}$  intervalli aperti, $h:I\to J$ $f:J\to\mathbb{R}$, continua siano parti $\alpha,\beta \in I$ allora vale:  
$\int _{h(\alpha)}^{h(\beta)} f(x)\space dx=\int_{\alpha}^{\beta}f(h(t))h'(t) \space dt$  
$x=h(t) \in J$= dominio di f


Considero $F,G: I \to \mathbb{R}$
$F(x)= \int_{h(\alpha)}^{h'(x)} f(x) dx, G(z) = \int_\alpha^z f(h(t))h'(t)\space dt$

Dimostro che $F \equiv G$


1. $F(\alpha)=G(\alpha)$
2. $F,G$ derivabile in $I$ e $F'(z)=G'(z) \forall z \in I$
 
$F(\alpha)=0, G(\alpha)=0$  
$G'(z)=f(h(z))h'(z) \forall z \in I$

$F'(z)=f(h(z))h'(z)\implies$ 2 vale e la tesi e dimostrata


## Integrale Generalizzato


Def: $F:[a,+\infty[ \to \mathbb{R}$, continua. Si dice $f$ integrabile in senso generalizzato su $[a,+\infty[$ se $\exists$ finito :

$\displaystyle \lim_{x \rightarrow \infty} \int_a^z f(x) dx = \int_a^{+\infty} f(x) dx$


$f::]-\infty,b] \to \mathbb{R}$ si fa $\displaystyle \lim_{x \rightarrow -\infty} \int_z^b f(x) \space dx$



Def $f:]a,b[\to \mathbb{R}$ continua.Dico f integrabile in $S,G$. se $\exists$ finito $\displaystyle \lim_{x \rightarrow 0_+}  \int_z^b f(x) \space dx= \int_a^b f(x) \space dx$


nel caso $f: [a,b[ \to \mathbb{R}$ continua $\int_a^b f(x) \space dx$ si definisca con $\displaystyle \lim_{x \rightarrow b-} \int_a^z f(x)\space dx$
