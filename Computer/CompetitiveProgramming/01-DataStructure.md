# DataStructure


## Set

versione con le hash `unordered_set` operazioni in $O(1)$ e set senza hash con $O(\log n)$


## Hash table

in c++ sono implementabili facilmente con `map` (tempo $O(\log n)$)o `unordered_map` (operzioni $O(1)$), unordered però può essere soggetta a problemi in qunato ci possono essere collisioni negli hash

## Segment tree

segment tree viene creato con 4n di spazio nella versione base si navaiga sapendo l'indice corente e il range di valori che i tiene
per esempio se i va da L a R i*2 va da L a (L+R)/2 e i*2+1 va da (L+R)/2+1 a R e si naviga così

**lazy update**: il lazy update serve nelle range query e updatare durante l'update quando ci si trova in un nodo che viene completamente compreso nel range si fa l'update e si flaggano i due nodi sotto come da updatare 
quando si fa una qualisi query che sia di update o per prendere valori quando si passa da un nodo flaggato si aggiorna e si flaggano i figli 



## Sum query

prefix sum array un array con la somma degli elementi precedenti con un costo di $O(n)$ per crearlo e $O(1)$ per le query

## Sparce table

si usa per una complessita $O(1)$ dopo un prepocessing di $O(n lg n)$ 
si puo usare per minimi e massimi o qualunque cosa che valga per un range in cui due array si intersecano (non una somma)
si calcola il log si creano tanti array quanti il log 
ogni array avrà una lunghezza di lenght+(1<<i)+1 dove i è il numero del array corrente
ogni cella dell i esimo array avrò valenza per (1<<i) celle dell'array origniario
per calcolare nel range i e j bisogna trovare la potenza di due che non eccede j-i+1 (chiamamola w) poi si prede l'array log(w) e si prendono i valori [log2(w)]\[i] e [log2(w)]\[j-w-1] 


## Merge sort tree

Il merge sort tree è come un segment tree ma ogni nodo ha un vettore che contiene tutti gli elementi ordinati.

<details>
<summary>
implementation
</summary>

**build**

```c++
vector<int>tree[5*N];
int A[N];
void build_tree( int cur , int l , int r )
{
     if( l==r )
     {
            tree[cur].push_back( a[ l ] );
            return ;
     }
     int mid = l+(r-l)/2;
     build_tree(2*cur+1 , l , mid ); // Build left tree 
     build_tree(2*cur+2 , mid+1 , r ); // Build right tree
     tree[cur] = merge( tree[2*cur+1] , tree[2*cur+2] ); //Merging the two sorted arrays
}
```

```c++
int query( int cur, int l, int r, int x, int y, int k)
{
       if( r < x || l > y )
      {
               return 0; //out of range
      }
      if( x<=l && r<=y )
      {
              //Binary search over the current sorted vector to find elements smaller than K

              Return lower_bound(tree[cur].begin(),tree[cur].end(),K)-tree[cur].begin();
      }
      int mid=l+(r-l)/2;
     return query(2*cur+1,l,mid,x,y,k)+query(2*cur+2,mid+1,r,x,y,k);
}
```

</details>

La build crea il tree in $O(n\log n)$ con spazio $O(n\log n)$



