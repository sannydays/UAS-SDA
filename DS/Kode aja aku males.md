int[] parent;
int[] size;
int[] rank;

int n; //jml elemen 

public DisjointSet(int n){
  this.n = n;
  parent = new int[n];
  size = new int[n];
  rank = new int[n];

  for(int i = 0; i < n; i++){
    makeSet(i);
  }
}

public void makeSet(int v){
  parent[v] = v;
  size[v] = 1;
  rank[v] = 0;
}

public int findSet(int v){
  if ( v == parent[v]){
  return v;
  }
  return parent[v] = findSet(parent[v]);
}

public void unionbySize(int a, int b){
  a = findSet(a);
  b = findSet(b);

  if(size[a] < size[b]){
    int temp = a;
    a = b;
    b = temp;
  }

    parent[b] = a;
    size[a] += size[b];
}

public void unionbyRank(int a, int b){
    a = findSet(a);
    b = findSet(b);

    if(a == b) return; 
    
    if(rank[a] < rank[b]){
        parent[a] = b;
    }else if(rank[a] > rank[b]){
        parent[b] = a;
    }else {
        parent[b] = a;
        rank[a]++;
    }
}



