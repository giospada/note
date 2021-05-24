# Grafi

[presentazione](https://wiki.olinfo.it/2021/grafi_visite_cammini.pdf)
[lezione Preoii](https://www.youtube.com/watch?v=LsbScEjDibA)

## BSF

- [ragnatela](https://training.olinfo.it/#/task/tecla/submissions)

[implementazione algoritmo](https://cp-algorithms.com/graph/breadth-first-search.html)

## DFS
- [Graph connettivity](https://onlinejudge.org/index.php?option=com_onlinejudge&Itemid=8&page=show_problem&category=0&problem=400&mosmsg=Submission+received+with+ID+26408465)


[implementazione algoritmo](https://cp-algorithms.com/graph/depth-first-search.html)

## Dijikstra

- [dijkstra](https://training.olinfo.it/#/task/dijkstra/statement)

[implementazione algoritmo](https://cp-algorithms.com/graph/dijkstra.html)


## Risorse

**alcuni Problemi con queste tecniche**

- [interruttori (terri)](https://territoriali.olinfo.it/task/interruttori)
- [Escursione (terri)](https://territoriali.olinfo.it/task/escursione)
- [TOE](https://www.spoj.com/problems/TOE1/)
- [TOE 2](https://www.spoj.com/problems/TOE2/)
- [trip](https://training.olinfo.it/#/task/ois_trip/statement)
- [disuguaglianze](https://training.olinfo.it/#/task/disuguaglianze/statement)
- [ropes](https://training.olinfo.it/#/task/ois_ropes/submissions)
- [barbablu](https://training.olinfo.it/#/task/barbablu/submissions)
- [maze](http://codeforces.com/contest/378/problem/C)
- [building roads](https://cses.fi/problemset/task/1666)


**Risorse per studiare**


- [visualizzatore di algoritmi](https://algorithm-visualizer.org/)
- [cp-algorithm per vedere la corretta implementazione di alcuni algoritmi](https://cp-algorithms.com/)
- [portale con problemi in categorie](https://cses.fi/problemset/)
- [tutti i problemi delle territoriali](https://training.olinfo.it/#/tasks/2?tag=territoriali) [quelli nuovi](https://territoriali.olinfo.it/)


### Esempi codice

##### BFS

```c++
#include <bits/stdc++.h>

using namespace std;


/**n è il numero di nodi
 * M è il numero di archi
 * a è un nodo e b è un nodo che hanno una relazione
 * N M
 * a b
 * a b
 *
 *
 */


vector<int> adj[1001];

bool done[1001];
int dist[1001];


int main(){
    const  int nodo_inizio=0;

    int N,M;
    cin >>N>>M;
    for(int i=0;i<M;i++){
        int a,b;
        cin >>a>>b;
        adj[a].push_back(b);
        adj[b].push_back(a);
    }
    for(int i=0;i<N;i++){
        done[i]=false;
        dist[i]=0;
    }

    //bfs
    //incominciamo dallo 0
    queue<int> q;
    q.push(nodo_inizio);
    done[nodo_inizio]=true; 
    dist[nodo_inizio]=0;
    while(!q.empty()){
        int node=q.front();
        q.pop();
        for(int i=0;i<adj[node].size();i++){
            int cur=adj[node][i];
            if(!done[cur]){
                q.push(cur);
                done[cur]=1;
                dist[cur]=dist[node]+1;
                cout <<cur<<" distanza "<<dist[cur]<<endl;
            }
        }
    }
    for(int i=0;i<N;i++){
        cout <<"il nodo "<<i<<" dista "<<dist[i]<<" dal nodo "<<nodo_inizio<<endl;
    }
}


```




```c++
//libreria che importa tutta la std
#include <bits/stdc++.h>
using namespace std;

//definiamo una costante
const int MN=10001;

// lista di adiacenza
vector<array<int,2>> v[MN];
//distanza da il nodo f a ogni nodo
long long dis[MN];

int main(){
//apriamo i file di input e output
    freopen("input.txt","r",stdin);
    freopen("output.txt","w",stdout);
    int n,m;
    //leggiamo n e m
    scanf("%d %d", &n,&m);
    int f,t;
    // leggiamo il nodo da cui partiamo e 
    // quello in cui dobbiamo arrivare
    scanf("%d %d", &f,&t);
    //nella nostra implementazione i 
    // nodi partiranno da 0
    //mentre nel problema incomiciano
    //con il valore di uno
    f--;t--;
    //legge tutti gli archi dall'input
    for(int i=0;i<m;i++){
        int a,b,c;
        scanf("%d %d %d",&a,&b,&c);
        //i nodi dell'input partono dall' uno
        //la nostra implementazione prevede che partino da 0
        a--;b--;
        //aggungiamo un legame a -> b
        // visto che il grafo è orientato
        // e visto che è pesato ci aggiungiamo il peso c
        v[a].push_back({b,c});
    }
    //setta il valore di dis(distanza) per tutti i nodi
    for(int i=0;i<n;i++){dis[i]=LONG_MAX;}
    // inizializza una priority queue
    //https://www.cplusplus.com/reference/queue/priority_queue/
    // la priority queue è una struttura dati che ci darà sempre l'elemento massimo
    //quindi mettiamo la distanza*-1 nella priority queue
    //così ci darà sempre il nodo con la minore distanza 
    priority_queue<array<long long,2>> pq;
    //aggiunge il nodo di inizio con 
    pq.push({0,f});
    //settiamo la distanza del punto di inizio a 0
    dis[f]=0;
    //funchè non ci sono più nodi da processare
    while(!pq.empty()){
        //prendiamo il nodo e la distanza
        array<long long,2> top=pq.top();
        pq.pop();
        //se la distanza è diversa dalla migliore andiamo avanti
        if(dis[top[1]]!=-top[0])continue;
        //se è il nodo che ci serviva smettiamo
        if(top[1]==t)break;
        //per ogni nodo da cui possiamo arrivare tramite top[1] che è il nodo corrente
        for(auto i: v[top[1]] ){
        //guardiamo se è minore la distanza da cui stiamo arrivando
        //rispetto a quella già salvata
            if(dis[i[0]]>i[1]-top[0]){
            //se è minore
            //aggiorniamo la distanza del nodo corrente 
                dis[i[0]]=i[1]-top[0];
                //aggiungiamo la distanza alla priority queue
                pq.push({-dis[i[0]],i[0]});
            }
        }
    }
    //scrive la distanza da f a t
    printf("%lld\n",dis[t]);
    
    
}

```
