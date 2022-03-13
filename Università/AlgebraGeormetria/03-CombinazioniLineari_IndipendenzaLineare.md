# Combinazioni Lineari Indipendenza Lineare


## Combinazione Lineare

Sia $V$ uno spazio vettoriale $v_1,\dots,v_n \in V$. Un vettore $v$ si dice combinazione lineare di $v_1,\dots,v_n$ se esistono $d_1,\dots,d_n\in\mathbb{R}$ tali che $v=d_1v_1+\dots+v_nd_n$

## Sottospazio Generato


**Sottospazio generato:** dato uno SV $V$ e un insieme di vettori $\{v_1,...\ v_n\}$ di $V$, il *sottospazio generato* dai vettori $v_1,...\ v_n$ è l'insieme di tutte le loro combinazioni lineari, che tradotto in simboli è: $\langle v_1,...\ v_n \rangle = \{ \lambda_1v_1 + ... + \lambda_nv_n\ |\ \lambda_1, ...\ \lambda_n \in \mathbb{R} \}$

> Nota: non l'ho capita

**Prop (3.1.5)** siano $V$ uno SV e  $\{v_1, ...\ v_n \}$ un insieme di vettori di $V$, si ha che $\langle v_1, ...\ v_n\rangle$ è un sottospazio vettoriale di $V$.

Inoltre se $Z$  è un sottospazio vettoriale di $V$  contenente $v_1,...\ v_n$, allora $\langle v_1, ...\ v_n\rangle  \subseteq Z$, cioè $\langle v_1, ...\ v_n\rangle$ è *il più piccolo* sottospazio vettoriale di $V$ contenente $v_1, ...\ v_n$.


**Prop (3.1.8):** dato un SV $V$, $v_1,...\ v_n \in V$ e $w$ una loro combinazione lineare, cioè $w = \lambda_1v_1+...+\lambda_n v_n$, allora: $\langle v_1, ...\ v_n\rangle = \langle v_1, ...\ v_n, w\rangle$
Vale anche il viceversa, ovvero se $\langle v_1, ...\ v_n\rangle = \langle v_1, ...\ v_n, w\rangle$ allora $w$ è combinazione lineare di $v_1 ...\ v_n$.

### Osservazioni

- il sottospazio generato da un singolo vettore dello SV $v \in V$ è l'insieme dei multipli di $v$, ovvero $\langle v  \rangle = \{ \lambda v\ |\ \lambda \in \mathbb{R} \}$
- il sottospazio generato dal vettore nullo invece è il sottospazio banale contenente solo il vettore nullo, ovvero $\langle 0 \rangle = \{ 0 \}$

**Generatori:** dato uno SV $V$ e un insieme di vettori di $V\ \{v_1, ...\ v_n \}$, si dice che $v_1,...\ v_n$ *generano $V$* o che  $\{v_1, ...\ v_n \}$ è un *insieme di generatori* di $V$ se $V = \langle v_1, ...\ v_n\rangle$.



### Nel piano Cartesiano


in $\mathbb{R}^2$  $<v>$ è una retta per $(0,0)$  

In $\mathbb{R}^3<v,w>$ è una retta appartiene $(0,0,0)$  



Sia $V$ spazio vetoriale $v_1,\dots,v_n \in V$ e $w= d_1v_1+\dots+d_nv_n$ allora $<v_1,\dots,v_n>=<v_1,\dots,v_n,w>$




## Linearmente indipendenti

**Def**: V spazio vettoriale $v_1,\dots,v_n\in V$ si dicono linearmente indipendenti se l'unica loro combinazione lineare che da $\underline{0}$ ()è quella con i coefficienti tutti nulli)

## Linearmente dipendenti

**Def** un insieme di vettori $v_1,\dots,v_n$ sono *linearmente dipendenti* $\exists d_1,\dots,d_n \in \mathbb{R}$  dove non sono tutti nulli tale che $d_1v_1+\dots+d_nv_n=\underline{0}$

**Oss**: se un insieme di vettori contiene $\underline{0}$ allora i vettori  sono (sempre) dipendenti


**prop(3.24)** sia V uno spazio vettoriale $v_1,\dots,v_n$ sono dipendenti $\iff$ almeno uno di essi è combinazione lineare degli altri
