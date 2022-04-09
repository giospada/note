# Grafi

## DFS

depth first search

<details>
<summary>
implementazione
</summary>

```cpp
vector<vector<int>> nodes;
vector<bool> done;

void dfs(int c){
    if(done[c])return;
    done[c]=true;
    for(auto t:nodes[c]){
        dfs(t);
    }
    
}

```

```cpp
vector<vector<int>> nodes;
vector<bool> done;

void dfs(int c){
    stack<int> st;
    while(!st.empty()){
        int c=st.top();
        done[c]=true;
        st.pop();
        for(auto t:nodes[c]){
            if(done[t])s.push(t);
        }
    }
}

```
</details>

## BFS


<details>
<summary>
implementazione
</summary>

```cpp

vector<vector<int>> nodes;
vector<bool> done;

void dfs(int c){
    queue<int> st;
    while(!st.empty()){
        int c=st.top();
        done[c]=true;
        st.pop();
        for(auto t:nodes[c]){
            if(done[t])s.push(t);
        }
    }
}
```

</details>



