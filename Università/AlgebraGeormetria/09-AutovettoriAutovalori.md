# Autovettori Autovalori

Sia $f: \mathbb{R}^n \to \mathbb{R}^n$, a F è associata a matrice $A=A_{\mathbb{C},\mathbb{C}}$ cambiando base, cambia la matrice associata $A_{\beta,\beta}=I^{-1}_{\beta,\mathbb{C}} A I_{\beta,\mathbb{C}}$, ci piacerebbe, cambiare la base ottenere una matrice diagonale.

$$
\begin{pmatrix}\lambda & 0 & 0 \\ 0 & \lambda  & 0 \\  0 & 0 & \lambda  \\ \end{pmatrix}
$$

> Nota: non è sempre possibile ottenerla

Se $A_{\beta,\beta}$ è diagonale, i vettori della base conservano la loro direzione


**Def:** Una applicazione lineare $F: \mathbb{R}^n \to \mathbb{R}^n$ si dice diagonalizzabile se esiste una base $\beta$ di $\mathbb{R}^n$ tale che $A_{\beta,\beta}$ sia diagonale

<details>
<summary>
esempio
</summary>

Esempio la simmetria rispetto alla retta x=y è diagonalizzabile

e la base è $\beta={e_1+e_2,-e_1+e_2}$

mentre in generale qualsiasi rotazione attorno all'origine, non è diagonalizzabile


</details>