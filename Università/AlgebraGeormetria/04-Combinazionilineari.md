# Combinazioni lineari e indipendenza lineare


## Combinazione lineare

**Combinazione lineare:** dato uno SV $V$ i cui vettori sono $v_1,...\ v_n$ e dati $\lambda_1,...\ \lambda_n \in \mathbb{R}$, il vettore $w = \lambda_1v_1+...+\lambda_n v_n$ si dice *combinazione lineare* di $v_1,...\ v_n$ con scalari $\lambda_1,...\ \lambda_n$.

Sottospazio generato: dato uno SV $V$ e un insieme di vettori $\{v_1,...\ v_n\}$ di $V$, il *sottospazio generato* dai vettori $v_1,...\ v_n$ è l'insieme di tutte le loro combinazioni lineari, che tradotto in simboli è: $\langle v_1,...\ v_n \rangle = \{ \lambda_1v_1 + ... + \lambda_nv_n\ |\ \lambda_1, ...\ \lambda_n \in \mathbb{R} \}$

Osservazioni:

- il sottospazio generato da un singolo vettore dello SV $v \in V$ è l'insieme dei multipli di $v$, ovvero $\langle v  \rangle = \{ \lambda v\ |\ \lambda \in \mathbb{R} \}$
- il sottospazio generato dal vettore nullo invece è il sottospazio banale contenente solo il vettore nullo, ovvero $\langle 0 \rangle = \{ 0 \}$

Generatori: dato uno SV $V$ e un insieme di vettori di $V\ \{v_1, ...\ v_n \}$, si dice che $v_1,...\ v_n$ *generano $V$* o che  $\{v_1, ...\ v_n \}$ è un *insieme di generatori* di $V$ se $V = \langle v_1, ...\ v_n\rangle$.

PROP: siano $V$ uno SV e  $\{v_1, ...\ v_n \}$ un insieme di vettori di $V$, si ha che $\langle v_1, ...\ v_n\rangle$ è un sottospazio vettoriale di $V$.

Inoltre se $Z$  è un sottospazio vettoriale di $V$  contenente $v_1,...\ v_n$, allora $\langle v_1, ...\ v_n\rangle  \subseteq Z$, cioè $\langle v_1, ...\ v_n\rangle$ è *il più piccolo* sottospazio vettoriale di $V$ contenente $v_1, ...\ v_n$.