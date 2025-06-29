| Perbedaan | DFS | BFS |
|---------|---------|---------|
| Cara Kerja | Menjelajah sedalam mungkin | Menjelajah seluruh tetangga|
| Struktur Data | Stack | Queue|
| Urutan | Child ke grandchild strsnya| Seluruh tetangga |
| Implementasi| Topological Sort | Shortest path |

Kompleksitasnya sama, yaitu O(V+E)

---
## DFS
```
create Stack
push(j)
mark as visited

while(!stack.isEmpty()){
 c = peek itu
  if (j has no adjacent)
  pop();
  else
  push(u) // tettangga si j
  mark as visited
}
```

## BFS
```
create Queue
enqueue(start)
mark start as visited

while (!queue.isEmpty()) {
    curr = queue.dequeue()

    for each unvisited neighbor u of curr {
        enqueue(u)
        mark u as visited
    }
}
```
