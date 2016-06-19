#COMP20007
Everything final examination


## SCC Strongly Connected components

For each vertex in SCC, there is a path to any other vertex in the SCC
![](http://rosalind.info/media/reverse.png)

**Source**: a vertex with no incoming edges
**Sink**: a vertex with no outgoing edges

<br />

## DFS
``` python
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

## DFS Edge Classification

![Screen Shot 2016-06-12 at 3.25.17 PM.png]()
<br />

## Pre and Post Number in DFS
Example
![](http://rosalind.info/media/directeddfsexample.png)
<br />

## Brute-force algorithm
Brute-force search or exhaustive search, also known as generate and test, is a very general problem-solving technique that consists of systematically enumerating all possible candidates for the solution and checking whether each candidate satisfies the problem's statement.
<br />

## Big O theta & big-omega
$f(x) = O(g(x))$ (big-oh)
means that the growth rate of f(x) is asymptotically _**less than or equal**_ to to the growth rate of $g(x)$

$f(x) = Ω(g(x))$ (big-omega)
means that the growth rate of f(x) is asymptotically _**greater than or equal**_ to the growth rate of $g(x)$

$f(x) = Θ(g(x))$ (theta)
means that the growth rate of f(x) is asymptotically _**equal**_ to the growth rate of $g(x)$
<br />

## heap (data structure)
A heap can be classified further as either a "max heap" or a "min heap". In a **max heap**, the keys of parent nodes are always greater than or equal to those of the children and the highest key is in the root node.
![Max heap](https://upload.wikimedia.org/wikipedia/commons/3/38/Max-Heap.svg)
<br />

### heap in an array
Parent position [$j/2$]
Children position [$2j$] & [$2j+1$]

## Matrix
<br />

### adjacency matrix
Space Complexity: $Θ(V^2)$
an adjacency matrix is a square matrix used to represent a finite graph. The elements of the matrix indicate whether **pairs of vertices are adjacent or not** in the graph.

![](https://wikimedia.org/api/rest_v1/media/math/render/svg/e8bcd9db7739c4cbc60a69f60ff1507d545fa039)
<br />

### incidence matrix
Space Complexity: $Θ(V*E)$
an incidence matrix is a matrix that shows the relationship between two classes of objects.
![](https://upload.wikimedia.org/wikipedia/commons/thumb/9/90/Labeled_undirected_graph.svg/445px-Labeled_undirected_graph.svg.png)
<br />

## Recurrence relations
A subproblems of size $n/b$ and then combining these answers in $O(n^d)$ time, for some $a,b,d > 0$ (in the multiplication algorithm, $a = 3$, $b = 2$, and $d = 1$). Their running time can therefore be captured by the equation $T(n) = aT([n/b]) + O(n^d).$
<br / >
![](/Users/wuxixiang/Desktop/Everything for Revising/resources/Pic3.png)

![](https://raw.githubusercontent.com/XixiangWu/Unimelb/master/Design%20of%20Algorithms/Everything%20for%20Revising/resources/Pic1.png
)

<br />

## Priortiy Queue
a priority queue is an abstract data type which is like a regular queue or stack data structure, but where **additionally each element has a "priority" associated with it**. In a priority queue, an element with high priority is served before an element with low priority. If two elements have the same priority, they are served according to their order in the queue.

![](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT_EB8XXkkEoLvmUhJ8FEA8TizZkX7taQuUJchEd4LAaJjsPulx)
<br />

## Euler Paths & Euler Circuit
An <font color="blue">Euler path</font>  is a path that uses every edge of a graph
exactly once.
An <font color="green">Euler circuit</font>  is a circuit that uses every edge of a graph
exactly once.

An **Euler path** starts and ends at <font color="blue">different</font>  vertices.
An **Euler circuit** starts and ends at the <font color="green">same</font>  vertex

![Screen Shot 2016-06-12 at 2.47.47 PM.png](https://raw.githubusercontent.com/XixiangWu/Unimelb/master/Design%20of%20Algorithms/Everything%20for%20Revising/resources/Pic4.png)

![Screen Shot 2016-06-12 at 2.47.57 PM.png](/Users/wuxixiang/Desktop/Everything for Revising/resources/Pic5.png)

<br />

## Cost in bits per symbol
* The data to be stored is called a **message**
* Each letter to be encoded is called a **symbol**
* Each bit pattern for each symbol is called a **codeword**
* A collection of **codewords** forms a **code**s
* We talk about “sending a message” and “storing some data” interchangeably. Storing data is just like sending it to disk.
* The cost of a code can be measured in bits-per-symbol, bps, for a particular message: total bits divided by the number of symbols
* ASCII always has the cost of 8 bps

<br />

## Shannon's entropy
If a symbol occurs with probability $p$, the best possible encoding for that symbol is $–log 2 p$

#### Static vs semi-static codes
ASCII and unary are examples of <font color="red">**a static code**</font>: it assigns the same codewords to symbols regardless of the message
A <font color="green">**semi-static**</font>  code knows the probability of occurrence of each symbol in the message

#### Shannon’s entropy theorem:
Given a message with n symbols each occurring $p_i$ times, the best bps possible is $H(p)=-\sum_{n}^{i=1}p_{i}log_{2}p_{i}$

The **inverse** of this is that a codeword of length x implies an expected probability of occurrence of $2^{-x}$

#### e.g. How to find the best semi-static code?

Message = ABAABBCAAABC
> $n=3$
symbols ${A, B, C}$
$p$ = {$\frac{6}{12}, \frac{4}{12} , \frac{2}{12}$}
$-log 2 (p)$ = {1, 1.6, 2.6}

We need a whole number of bits per codeword, and we need unique decipherability

#### e.g. How to build a semi-static prefix code?
Message = ABAABBCAAABC
> $n=3$
symbols ${A, B, C}$
$p$ = {$\frac{6}{12}, \frac{4}{12} , \frac{2}{12}$}
$-log 2 (p)$ = ${1, 1.6, 2.6}$
code = {$0, 10, 11$}
bps = $(6*1 + 4*2 + 2*2)/12 = 1.5$

![](/Users/wuxixiang/Desktop/Everything for Revising/resources/Screen Shot 2016-06-13 at 4.38.49 PM.png
)

#### Shannon-Fano algorithm
Divide in half and join recursively
![](/Users/wuxixiang/Desktop/Everything for Revising/resources/Screen Shot 2016-06-13 at 4.41.12 PM.png)
<br />

## Huffman encoding
![](/Users/wuxixiang/Desktop/Everything for Revising/resources/Screen Shot 2016-06-13 at 4.51.11 PM.png
)

#### Bounds
for an N symbol message, the codewords can be at most (log φ N) − 1 ≈ (1.44 log 2 N) − 1 bits long.

#### Complexity
O(n) time and O(n) space, once the weights are **sorted**

<br />	

## Greedy Algorithms Definition
A greedy algorithm is an algorithm that follows the problem solving heuristic of making the locally optimal choice at each stage[1] with the hope of finding a global optimum.

<br />

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

## Prim's Algorithm
Mimum spanning tree
![](https://upload.wikimedia.org/wikipedia/commons/thumb/f/f7/Prim%27s_algorithm.svg/240px-Prim%27s_algorithm.svg.png)

#### Complexity
Where **E** is the number of edges in the graph and **V** is the number of vertices, Kruskal's algorithm can be shown to run in **O(E log E)** time, or equivalently, <font color="red">**O(E log V)**</font> time, all with simple data structures.

## Dijkstra's Algorithm (find shortest path)
Complexity: O((V+E)log V)
![](https://upload.wikimedia.org/wikipedia/commons/5/57/Dijkstra_Animation.gif)
## Bellman-Ford algorithm 
find shortest path when negative edge exists

![](/Users/wuxixiang/Desktop/Everything for Revising/resources/4.png
)

## RSA
c = encrypted data
d = private key
n = public key
Decrypted Data = $c^d$ mod n


