## Pengertian Graph
Struktur data yang terdiri oleh node (simpul/vertex) dan edge (sisi) yang mewakili hubungan antar data.
Fyi: 
#### Path merupakan barisan titik (node) yang dihubungkan oleh edge.
#### Simple Path: Node hanya muncul 1 kali.
#### Cycle -> jalur yang dimulai dan berakhir pada node sama
#### Simple cycle -> kayak cycle tapi node yg sama hanya muncul 1x diakhir dan awal. Selain itu beda.
---
## Jenis-Jenis Graph
### 1. Directed Graph 
Directed graph merupakan jenis graph yang setiap sisi (edge)nya merupakan directed edge (memiliki arah). Memiliki:
  a. Successor : Penerus
  b. PreSuccessor : Pendahulu
  c. Adjacent : Tetangga yang terghubung langsung.
### 2. Connected Graph
Dari setiap node yang berbeda dalam graph memiliki jalur antar pasangan.
### 3. Disconnected Graph
Terputus. Jika disconnect maka graph dapat dipartisi menjadi beberapa subgraph supaya setiap graphnya terhubung connected komponen.
### 4. Complete Graph
Setiap pasangan node memiliki edge
### 5. Subgraph
Bagian dari graph yang dibentuk oleh sejumlah simpul dan edge dari graph asal tanpa menambahkan yang baru.
### 6. Weighted Graph
Graph yang setiap edgenya memiliki bobot.
### 7. Multigraph
Graph yang boleh duplikat edge dan bisa self edge (loop) jadi edge antar node itu boleh > 1.
---
## Apakah Graf == Tree???
Graf tidak sama dengan tree, tetapi bisa direpresentasikan dengan tree. Terus gimana? 
1. Undirected
2. Connected
3. Tidak cycle
---
### Representasi Graph
1. Adjacency Matrix -> Pakai array 2D dengan ukuran jumlah node^2
2. Adjacency List -> Tiap simpul (node) menyimpan daftar simpul lain yang terhubung langsung
