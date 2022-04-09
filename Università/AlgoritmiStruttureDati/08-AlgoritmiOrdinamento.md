# Algoritmi Ordinamento

**Tipi di Ordinamento:**
- **in loco:** utilizza lo stesso array solamente cambiando le posizione
- **stabile**: gli elementi con la stessa chiave rimangono nello stesso ordine


## Selection Sort

**funzionamento**: **ricerca il minimo** in tutto l'array tranne la parte che è già stata ordinata e lo **scambia con il primo elemenento** della parte non ordinata, il primo elemento della parte non ordinata ora è in ordine e quindi diventa parte della parte ordinata e ricomincia


<details>
<summary>
implementazione
</summary>

```java
public static void selectionSort(Comparable A[]) {
    for (int k = 0; k < A.length - 1; k++) {
    // cerca il minimo A[m] in A[k..n-1]
    int m = k;
    for (int j = k + 1; j < A.length; j++)
        if (A[j].compareTo(A[m]) < 0)
            m = j;
        // scambia A[k] con A[m]
        if (m != k) {
            Comparable temp = A[m];
            A[m] = A[k];
            A[k] = temp;
        }
    }
}
```

</details>


**Costo computazionale**:$\Theta(n^2)$

## Insertion Sort

**funzionamento**: tiene una parte ordinata e una non ordinata, prende il primo elemento della parte non ordinata e lo inserisce ordinandolo nella parte ordinata

<details>
<summary>
implementazione
</summary>

```java
public static void insertionSort(Comparable A[]) {
    for (int k = 1; k <= A.length - 1; k++) {
        int j;
        Comparable x = A[k];
        // cerca la posizione j in cui inserire A[k]
        for (j = 0; j < k; j++)
        if (A[j].compareTo(x) > 0) break;
        if (j < k) {
            // Sposta A[j..k-1] in A[j+1..k]
            for (int t = k; t > j; t--)
                A[t] = A[t – 1];
            // Inserisci A[k] in posizione j
            A[j] = x;
        }
    }
}
```
</details>


**Costo computazionale**:$\Theta(n^2)$

## Bubble Sort

**funzionamento**: intera l'array finchè non è ordinato, ogni volta che trova un elemento minore di quello che segue li swappa e continua a ciclare


<details>
<summary>
implementazione
</summary>

```java
public static void bubbleSort(Comparable A[]) {
    for (int i = 1; i < A.length; i++) {
        boolean scambiAvvenuti = false;
        for (int j = 1; j <= A.length - i; j++) {
        // Se A[j-1] > A[j], scambiali
            if (A[j - 1].compareTo(A[j]) > 0) {
                Comparable temp = A[j - 1];
                A[j - 1] = A[j];
                A[j] = temp;
                scambiAvvenuti = true;
            }
        }
    if (!scambiAvvenuti) break;
    }
}
```
</details>



**Costo computazionale**:$\Theta(n^2)$

## Quick Sort

**funzionamento**:
- divide: divide l'array in due parti in cui una contiene gli elementi più piccoli del pivot e l'altra gli elementi più grandi del pivot
- impera: combina i due sotto array chimando quicksort ricorsivamente 
- combina: i due sottoarray sono già ordinati


**funzionamento (partition)**: Manteniamo due indici, inf e sup, che vengono fatti scorrere dalle estremità del vettore verso il centro

<details>
<summary>
implementazione
</summary>

```java
public static void quickSort(Comparable A[]) {
    quickSortRec(A, 0, A.length - 1);
}

public static void quickSortRec(Comparable A[], int i, int f) {
    if (i >= f) return;
    int m = partition(A, i, f);
    quickSortRec(A, i, m - 1);
    quickSortRec(A, m+1, f);
}


private static int partition(Comparable A[], int i, int f) {
    int inf = i, sup = f + 1;
    Comparable temp, x = A[i];
    while (true) {
        do {
            inf++;
        } while (inf <= f && A[inf].compareTo(x) <= 0);
        do {
            sup--;
        } while (A[sup].compareTo(x) > 0);
        if (inf < sup) {
            temp = A[inf];
            A[inf] = A[sup];
            A[sup] = temp;
        } else break;
    }
    temp = A[i];
    A[i] = A[sup];
    A[sup] = temp;
    return sup;
}

```
</details>

**Costo di ordinamento** peggiore $\Theta (n^2)$ (scegliendo come pivot il numero più piccolo), migliore  $\Theta (n \log n)$ (scegliendo il numero che divide in esattamente due array)


## Marge Sort

**funzionamento**:
- divide: si divide l'array a metà
- impera:si chima la procedura su entrambe le metà partizionate
- combina:gli array sono ordinati perchè abbiamo chiamato il merge sort quindi li mergiamo togliendo il più piccolo dai due e mettendolo nella prima posizione


<details>
<summary>
implementazione
</summary>

```java
public static void mergeSort(Comparable A[]) {
    mergeSortRec(A, 0, A.length - 1);
}

private static void mergeSortRec(Comparable A[], int i, int f) {
    if (i >= f) return;
    int m = (i + f) / 2;
    mergeSortRec(A, i, m);
    mergeSortRec(A, m + 1, f);
    merge(A, i, m, f);
}

private static void merge(Comparable A[], int i1, int f1, int f2) {
    Comparable[] X = new Comparable[f2 - i1 + 1];
    int i = 0, i2 = f1 + 1, k = i1;
    while (i1 <= f1 && i2 <= f2) {
        if (A[i1].compareTo(A[i2]) < 0)
            X[i++] = A[i1++];
        else
            X[i++] = A[i2++];
    }
    if (i1 <= f1)
        for (int j = i1; j <= f1; j++, i++) X[i] = A[j];
    else
        for (int j = i2; j <= f2; j++, i++) X[i] = A[j];
    for (int t = 0; k <= f2; k++, t++) A[k] = X[t];
}
```

</details>


**costo computaizonale**: $\Theta (n \log n)$ (metodo dell'esperto $T(n)=2T\Bigl(\frac{n}{2}\Bigr)+n$)


## HeapSort


Crea una max heap con in $O(n)$ poi per elminima l'elemento più grande e ristabilisce la heap, inserisce l'lemento appena tolto infondo  $O(\log n)$(nella parte che non è più nella heap) finchè la heap non è vuota.


**costo computaizonale**: $\Theta (n \log n)$ 


## Counting Sort

Può essere utilizzato solo su un array contentente valori da 0 a k, conta la ricorrenza di ogni elemento in un array di dimensione k.

<details>
<summary>
implementazionoe
</summary>

```java
public static void countingSort(int[] A, int k) {
    int[] Y = new int[k];
    int j = 0;
    for (int i = 0; i < k; i++) Y[i] = 0;
    for (int i = 0; i < A.length; i++) Y[A[i]]++;
    for (int i = 0; i < k; i++) {
        while (Y[i] > 0) {
            A[j] = i;
            j++;
            Y[i]--;
        }
    }
}
```

</details>


**costo computazionale** $O(n+k)$


##  Bucket Sort

Bucket sort è come il counting, ma al posto di contare i valori si tiene una linked list che contiene tutti i gli oggetti da ordinare

**costo computazionale**: $O(n+k)$


## Radix Sort
















