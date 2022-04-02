# Calcolo Dei Minimi E Massimi

## Matrice Jacobiana


È un modo per scrivere il gradiente di una funzione quando è in una certa forma.

Data una funzione $f: \mathbb{R}^n \to \mathbb{R}^p$

ossia per esempio $x=(x_1,...,x_n) \to(f_1(x),...,f_p(x))$

Se le p funzioni di arrivo sono differenziabili, allora la matrice jacobiana è definita in questo modo:

$J_f(x) = \begin{pmatrix} \delta_{x_1} f_1(x) & ... & \delta_{x_n} f_1(x)\\ \vdots & \vdots & \vdots \\ \delta_{x_1} f_p(x) & ... & \delta_{x_n} f_p(x) \end{pmatrix}$ 

Una matrice con p righe e n colonne, che rappresentano **tutte le derivate parziali possibile**

**Osservazione**

Da una funzione differenziabile f(r(x)) in modo simile a quanto fatto prima, abbiamo che 

$J_f(r(t)) J_r(t)$ è uguale al prodotto scalare!

$(\delta_1f(r(t)), ..., \delta_nf(r(t))) \cdot \begin{pmatrix} \delta_{s} r_1(t) \\ \vdots \\ \delta_{s} r_n(t) \end{pmatrix}$

Ossia è proprio $\delta_t(f(r(t))$ il prodotto scalare, ossia $J_{f \cdot r}(t)$ e la cosa bella è che **vale per dimensione qualsiasi**. (vedere gli appunti lezione 11, ci dovrebbe essere l'enunciato di questo).