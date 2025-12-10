---

# 🟩 **UNIT–4: TREES AND GRAPHS (FULL NOTES)**

---

# ⭐ **1. Introduction to Trees**

Tree ek **non-linear hierarchical data structure** hota hai jisme nodes parent-child relation me arranged hote hain.

### ⚡ Key Terms:

* **Node** → Single element
* **Root** → Top-most node
* **Parent** → Jo kisi node ko point kare
* **Child** → Parent ke neeche
* **Leaf** → Jiske aage koi child nahi
* **Siblings** → Same parent ke nodes
* **Depth** → Root se niche ki level
* **Height** → Longest path to leaf
* **Degree** → Children count of node
* **Forest** → Multiple disjoint trees

---

# ⭐ **2. Binary Tree**

Binary tree me **max 2 children** allowed hote hain — left child & right child.

### Types:

1. **Full Binary Tree**
   → Har node ya to 0 ya 2 children.

2. **Complete Binary Tree**
   → Saare levels filled left to right.

3. **Perfect Binary Tree**
   → Har level completely filled.

4. **Skewed Tree**
   → All nodes only left OR right.

---

# ⭐ **3. Binary Tree Traversals**

Traversal means every node ko visit karna.

### ✔ **1. Preorder (Root → Left → Right)**

```
Visit root
Traverse left subtree
Traverse right subtree
```

### ✔ **2. Inorder (Left → Root → Right)**

→ BST ka inorder hamesha sorted deta hai.

### ✔ **3. Postorder (Left → Right → Root)**

### ✔ **4. Level Order Traversal**

→ BFS use karta hai (queue).

---

# ⭐ **4. Binary Search Tree (BST)**

### ✔ BST Property

```
Left subtree < Root < Right subtree
```

### ✔ Operations:

#### 1. **Search:**

* Root se start
* Agar value < root → left jao
* Agar value > root → right jao
* Found → return node

**Time:**

* Best: O(log n)
* Worst (skewed): O(n)

#### 2. **Insertion:**

Same as search → jaha NULL mile waha insert.

#### 3. **Deletion:**

Three cases:

1. **Node is leaf**
   → Direct delete

2. **Node has 1 child**
   → Child ko parent se link karo

3. **Node has 2 children**
   → Inorder successor/Predecessor find
   → Replace → Delete duplicate node

---

# ⭐ **5. Tree Representation**

### ✔ Using Arrays

Only complete binary tree me best.

Parent-child relations:

```
Left Child  = 2*i
Right Child = 2*i + 1
Parent      = i/2
```

### ✔ Using Linked List (Pointer Representation)

```
struct node {
    int data;
    node *left;
    node *right;
};
```

---

# ⭐ **6. Graphs**

Graph = Nodes + Edges

### ✔ Types of Graph:

* **Directed (digraph)**
* **Undirected**
* **Weighted**
* **Unweighted**
* **Cyclic / Acyclic**
* **Connected / Disconnected**

### ⚡ Terminology:

* **Vertex (V)** → Nodes
* **Edge (E)** → Connections
* **Degree** → Adjacent edges count
* **Path** → Sequence of nodes
* **Cycle** → Start and end same
* **Adjacency** → Connected or not

---

# ⭐ **7. Graph Representation**

---

## 🔵 **1. Adjacency Matrix**

* 2D matrix of size V × V
* 1 = edge exists, 0 = no edge

**Pros:** Fast edge check
**Cons:** Space waste if sparse

---

## 🔵 **2. Adjacency List**

* Har vertex ka ek linked list of neighbors

**Pros:** Space efficient
**Cons:** Edge check slow

---

# ⭐ **8. Graph Traversal Algorithms**

---

## 🔵 **DFS (Depth First Search)**

→ Stack/Recursion use hota hai.

**Process:**

1. Start at node
2. Mark visited
3. Child pe recursively call
4. Backtrack when no unvisited child

**Use:** Cycle detection, Topological sort

**Time Complexity:** O(V + E)

---

## 🔵 **BFS (Breadth First Search)**

→ Queue use hota hai.

**Process:**

1. Start at node
2. Queue me push
3. Level by level visit

**Use:** Shortest path (unweighted graph)

**Time Complexity:** O(V + E)

---

# ⭐ **9. Spanning Tree (Basic)**

* Graph ka aisa tree jisme **all vertices included**
* No cycles
* For connected graph only

**Minimum Spanning Tree Algorithms:**

* Kruskal
* Prim

(If needed can give full algorithm)

---

# ⭐ **10. Applications of Trees & Graphs**

* File system hierarchy
* Folder structure
* BST in searching
* Network routing graph
* Social network graph connections
* Google Maps shortest path (BFS/Dijkstra)

---

# ⭐ **Important Exam Questions (Unit–4)**

📌 Difference: Tree vs Binary Tree vs BST
📌 Write algorithms for Preorder, Inorder, Postorder
📌 Construct BST from given sequence
📌 Adjacency matrix vs list compare
📌 DFS & BFS algorithm + time complexity
📌 Different types of binary trees
📌 Height & depth difference
📌 Delete node from BST
📌 Types of graphs

---
