# Sistemi Lineari


## Contro Immagine

**Def:**(controimmagine)Sia $F:V\to W$ un'applicazione lineare e sia $w\in W$, si chiama controimmagine o preimmagine di $w$ mediante $F$ l'insieme $F^{-1}( w)=\{ v\in V|F(v)=w\}$, la notazione $F^{-1}$ non ha nulla a che fare con l'invertibilità della funzione, indica semplicemente un sottoinsieme del dominio della funzione

**Prep** 6.1.4: sia $F:V\to W$ un'applicazione lineare e sia $w \in W, \space F^{-1}( w)\neq \emptyset \iff w \in Im\ F$ in tal caso si ha $F^{-1}( w)=\{ v + z| z \in\ker F\}$ ove $v$ è un qualsiasi elemento di V tale che $F( v)= w$


**Def**: Sia $A \in M_{m,n}(\mathbb{R})$ , $rr(A)=\dim(<\text{righe di A}>)$, $rc(A)= \dim(<\text{colonne di A}>)$


**Prep**(6.2.3): Se $A \in M_{nmn}(\mathbb{R})$ allora $rr(A)=rc(A)$


## Teorema di Rouchè-Capelli


Sia $Ax=b$ un sinstema lineare pazzo manifesto di m equazioni in n incognite (cioè $A\in M_{n,m}(\mathbb{R})$), ammette soluzioni solo se  $rg(A)=rg(A|b)$.Se tale uguaglianza è soddisfatta, allora il sistema ha:
1. una sola soluzione se e solo se $rg(A)=rg(A|b)=n$
2. infinite soluzioni se e solo se $rg(A)=rg(A|b)<n$. In tal caso le soluzioni del sistema dipendono da $n-rg(A)$ parametri
