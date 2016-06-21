## Brute-force algorithm
Brute-force search or exhaustive search, also known as generate and test, is a very general problem-solving technique that consists of systematically enumerating all possible candidates for the solution and checking whether each candidate satisfies the problem's statement.

<br />

---

## Big O theta & big-omega
$f(x) = O(g(x))$ (big-oh)
means that the growth rate of f(x) is asymptotically _**less than or equal**_ to to the growth rate of $g(x)$

$f(x) = Ω(g(x))$ (big-omega)
means that the growth rate of f(x) is asymptotically _**greater than or equal**_ to the growth rate of $g(x)$

$f(x) = Θ(g(x))$ (theta)
means that the growth rate of f(x) is asymptotically _**equal**_ to the growth rate of $g(x)$

<br />

---

## heap (data structure)
A heap can be classified further as either a "max heap" or a "min heap". In a **max heap**, the keys of parent nodes are always greater than or equal to those of the children and the highest key is in the root node.
<img src="https://upload.wikimedia.org/wikipedia/commons/3/38/Max-Heap.svg" style="width: 200px;"/> 

<br />

---

## Matrix

### adjacency matrix
Space Complexity: $Θ(V^2)$
an adjacency matrix is a square matrix used to represent a finite graph. The elements of the matrix indicate whether **pairs of vertices are adjacent or not** in the graph.

![](https://wikimedia.org/api/rest_v1/media/math/render/svg/e8bcd9db7739c4cbc60a69f60ff1507d545fa039)

<br />

### incidence matrix
Space Complexity: $Θ(V*E)$
an incidence matrix is a matrix that shows the relationship between two classes of objects.
<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/9/90/Labeled_undirected_graph.svg/445px-Labeled_undirected_graph.svg.png" style="width: 200px;"/> 
<br />

---


## Recurrence relations
$a$ subproblems of size $n/b$ and then combining these answers in $O(n^d)$ time, for some $a,b,d > 0$ (in the multiplication algorithm, $a = 3$, $b = 2$, and $d = 1$). Their running time can therefore be captured by the equation $T(n) = aT([n/b]) + O(n^d).$
<br / >
![Screen Shot 2016-05-01 at 4.02.25 PM.png](resources/593B73C99B14AE760AC67ADDAC00359E.png)
![Screen Shot 2016-05-01 at 4.16.31 PM.png](resources/0AD57D2AE928C81C814B8FA2474CDC06.png)

<br />

---

## Priortiy Queue
a priority queue is an abstract data type which is like a regular queue or stack data structure, but where **additionally each element has a "priority" associated with it**. In a priority queue, an element with high priority is served before an element with low priority. If two elements have the same priority, they are served according to their order in the queue.

![](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT_EB8XXkkEoLvmUhJ8FEA8TizZkX7taQuUJchEd4LAaJjsPulx)

<br />

---


## Euler Paths & Euler Circuit
An <font color="blue">Euler path</font>  is a path that uses every edge of a graph
exactly once.
An <font color="green">Euler circuit</font>  is a circuit that uses every edge of a graph
exactly once.

An **Euler path** starts and ends at <font color="blue">different</font>  vertices.
An **Euler circuit** starts and ends at the <font color="green">same</font>  vertex

<img src="resources/DC62F1DC879EEBAEF2BED38D11EDFD58.png" style="width: 400px;"/> 
<img src="resources/F7B29598B8FDB0A0210B0BDFD1EE41BC.png" style="width: 400px;"/> 

<br />

---

# Data Compression

## Huffman encoding

![Huffman encoding.png](resources/85F9FAA8E035F90393C6FF4269B1E90B.png)

### Cost in bits per symbol
* The data to be stored is called a **message**
* Each letter to be encoded is called a **symbol**
* Each bit pattern for each symbol is called a **codeword**
* A collection of **codewords** forms a **code**s
* We talk about “sending a message” and “storing some data” interchangeably. Storing data is just like sending it to disk.
* The cost of a code can be measured in bits-per-symbol, bps, for a particular message: total bits divided by the number of symbols
* ASCII always has the cost of 8 bps


<p align="center">$bps = \frac{total bits}{the number of symbols}$</p> 

<br />

---
## Shannon-Fano coding

![Shannon fano.png](resources/4226BBA6931106BEE04594D509474AAF.png)

## Shannon's entropy
If a symbol occurs with probability $p$, the best possible encoding for that symbol is
<p align="center">$ –log 2 p$</p> 

<br />

---

### Shannon’s entropy theorem:
Given a message with n symbols each occurring p i times, the best bps possible is

\begin{align}
H(p)=-\sum_{n}^{i=1}p_{i}log_{2}p_{i}
\end{align}

<br />

---

# Graph

## DAG (Directed acyclic graph)
a finite directed graph with no directed cycles
<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/c/c6/Topological_Ordering.svg/440px-Topological_Ordering.svg.png" style="width: 200px;"/> 

<br />

---

## SCC Strongly Connected components

For each vertex in SCC, there is a path to any other vertex in the SCC
![](http://rosalind.info/media/reverse.png)

**Source**: a vertex with no incoming edges
**Sink**: a vertex with no outgoing edges

<br />

---

## BFS Breath-fisrt Search

![](https://upload.wikimedia.org/wikipedia/commons/4/46/Animated_BFS.gif)

### Complexity: 
<p align="center">$O (V+E)$</p> 

<br />

---


## DFS Depth-first Search

### Complexity: 
<p align="center">$O (V+E)$</p> 

### Pseudo code
``` c
traverse(v): 
    s = stack
    s.push(v) 
    while s not empty: 
        v = s.pop()
        mark v visited
        for each w adjacent to v:
            if w not visited:
                s.push(w)
```
<br />

---


## DFS Edge Classification

![Screen Shot 2016-06-12 at 3.25.17 PM.png](resources/4DD0E9465549BBC7C3500E785635E996.png)

<br />

---

## Pre and Post Number in DFS
Example
![](http://rosalind.info/media/directeddfsexample.png)

<br />

---


## Greedy Algorithms Definition
A greedy algorithm is an algorithm that follows the problem solving heuristic of making the locally optimal choice at each stage with the hope of finding a global optimum.

<br />

---

## Kruskal's Algorithm
![](https://upload.wikimedia.org/wikipedia/commons/thumb/5/5c/MST_kruskal_en.gif/400px-MST_kruskal_en.gif)

``` python
KRUSKAL(G):
A = ∅
foreach v ∈ G.V:
	MAKE-SET(v)
foreach (u, v) in G.E ordered by weight(u, v), increasing:
if FIND-SET(u) ≠ FIND-SET(
	A = A ∪ {(u, v)}
	UNION(u, v)
return A
```

<br />

---

## Prim's Algorithm
Mimum spanning tree

<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/f/f7/Prim%27s_algorithm.svg/240px-Prim%27s_algorithm.svg.png" style="width: 100px;"/>

<br />

#### Complexity
Where **E** is the number of edges in the graph and **V** is the number of vertices, Kruskal's algorithm can be shown to run in **O(E log E)** time, or equivalently, <font color="red">**O(E log V)**</font> time, all with simple data structures.

<br />

---

## Dijkstra's Algorithm (find shortest path)
Complexity: O((V+E)log V)
![](https://upload.wikimedia.org/wikipedia/commons/5/57/Dijkstra_Animation.gif)

<br />

---

## Bellman-Ford algorithm 
find shortest path when negative edge exists

![Bellman-Ford.png](resources/0DB34A6B35A2B80C1629DFEEF24D9F24.png)

<br />

---

## Knapsack Problem


<br />

---



## Disjoint Set
It is a data structure that keeps track of a set of elements partitioned into a number of disjoint (nonoverlapping) subsets.
* _Find_: Determine which subset a particular element is in.
* _Union_: Join two subsets into a single subset.


<p align="center"> <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/6/67/Dsu_disjoint_sets_init.svg/720px-Dsu_disjoint_sets_init.svg.png" style="width: 400px;"/>
<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/a/ac/Dsu_disjoint_sets_final.svg/720px-Dsu_disjoint_sets_final.svg.png" style="width: 400px;"/> </p> 

### Complexity
* makeset $O(1)$
* find worst $O(V)$
* union $O(1)$

<br />

---

## Kahn's Algorithm
``` c
function toposort_kahn

    input: V and E in graph G (a dag)
    output: x - the topological sorted vertices

    q = a queue with all vertices having no incoming edge // O(V)
    x = an empty linked list

    while q is not empty

        v = q.dequeue() // O(1) * O(V) times
        x.append(v) // O(1) * O(V) times

        for e, u in outgoing edges of v such that e(v,u)
            delete e // O(1) * O(E) times
            if u doesn't have any incoming edge // O(1) * O(E) times
                q.enqueue(u) // O(1) * O(E) times
                
    via Xiao Liang Yu
```

### Complexity
Time Complexity: $O(V+E)$

<br />

---

## Comparison Sort
A **comparison** sort is a type of sorting algorithm that only reads the list elements through a single abstract comparison operation (often a "less than or equal to" operator or a three-way comparison) that determines which of two elements should occur first in the final sorted list.

<br />

---
# Hashing


<br />

---

# Secret Sharing

## Dynamic Programming

<br />

---

## RSA
c = encrypted data
d = private key
n = public key
Decrypted Data = $c^d$ mod n

<br />

---

## Number Theory

### Modular arithmetic

(A $*$ B) mod C = (A mod C $*$ B mod C) mod C

(A + B) mod C = (A mod C + B mod C) mod C

$A^B$ mod C = ((A mod C)$^B$ mod C

<br />

---

# NP/P/NP-Completeness

## K-th smallest algorithm