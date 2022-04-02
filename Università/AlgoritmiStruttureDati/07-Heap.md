# Heap

Heap è una struttura dati che riesce a mantenere il massimo, attraverso un binary tree.

Le heap possono essere di due tipi:
- **max-heap:** tutti i nodi padri di un figlio sono maggiori dei figli
- **min-heap:** tutti i nodi padri di un figlio sono minori dei figli

**operazioni**:
- `insert`: inserisce un elemento
- `build`: crea l'albero
- `getMax/getMin`: ritorna il massimo/minimo
- `fixHeap`: se la proprietà di heap non è rispettata la ripristina
- `removeMax/removeMin`: rimove il massimo/minimo

## Implementazione con Array

Si tiene un array tale che:
- A[1] contiene la radice (quindi il minimo o il massimo)
- parent(i) è definito come $\lfloor i\rfloor$
- left(i) è definito come $i*2$
- right(i) è definito come $i*2+1$

### Operazioni

`build`: crea l'albero in $\Theta(n)$

<details>
<summary>
implementazione
</summary>

```java
private static void heapify(Comparable S[], int n, int i) {
    if (i > n) return;
    heapify(S, n, 2 * i); // crea heap radicato in S[2*i]
    heapify(S, n, 2 * i + 1); // crea heap radicato in S[2*i+1]
    fixHeap(S, n, i);
}
// per trasformare un array S in uno heap:
// heapify(S, S.length, 1 );
```
</details>


`insert`: inserisce un elemento

`getMax/getMin`: ritorna il massimo/minimo

`fixHeap`: se la proprietà di heap non è rispettata la ripristina

<details>
<summary>
implementazione
</summary>

```java
private static void fixHeap(Comparable S[], int c, int i) {
    int max = 2 * i; // figlio sinistro
    if (2 * i > c) return;
    if (2 * i + 1 <= c && S[2 * i].compareTo(S[2 * i + 1]) < 0)
    max = 2 * i + 1; // figlio destro
    if (S[i].compareTo(S[max]) < 0) {
        Comparable temp = S[max];
        S[max] = S[i];
        S[i] = temp;
        fixHeap(S, c, max);
    }
}
```
</details>

`removeMax/removeMin`: rimove il massimo/minimo, consinste eliminare il massimo e il minimo mette al suo posto l'ultimo elemento nell'array e chiama fixheap
