# ⭐ **UNIT 1 – INTRODUCTION (EXTREME DEPTH – FULL EXPANDED VERSION)**

(Every topic at maximum exam depth)

---

# **1. Basic Terminologies**

Data Structure = **Organized collection of data** + operations.

### ⭐ Data Structure = *WHAT + HOW*

* **WHAT** data store karna hai
* **HOW** store karna hai efficiently

---

# **1.1 Data Types (Very Important for 3 Marks)**

### ✔ Primitive Data Types

Computer ke sabse basic data units:

| Type  | Description | Example   |
| ----- | ----------- | --------- |
| int   | Integer     | 1, 2, 300 |
| float | Decimal     | 3.14      |
| char  | Character   | 'A'       |
| bool  | Boolean     | true      |

### ✔ Why needed?

Because primitive types → **building blocks** of all DS.

---

# **1.2 Non-Primitive Data Types**

### ✔ Linear

Elements ek straight line me arranged:

```
A → B → C → D
```

Types:

* Array
* Linked List
* Stack
* Queue

### ✔ Non-Linear

Hierarchy + relationships:

```
        A
      /   \
     B     C
```

Types:

* Tree
* Graph
* Hash table (mix of both ideas)

---

# **1.3 Key Data Structure Operations (MOST IMPORTANT – 5 Marks)**

Exam me direct aata hai:
**“Explain basic operations on data structures.”**

### ⭐ (1) Traversal

Har element ko ek baar visit karna
→ Time = **O(n)**

### ⭐ (2) Insertion

New data add karna.

| DS                           | Insertion Time |
| ---------------------------- | -------------- |
| Array end                    | O(1)           |
| Array middle                 | O(n)           |
| Linked List at start         | O(1)           |
| LL at middle (after pointer) | O(1)           |
| Stack Push                   | O(1)           |

### ⭐ (3) Deletion

Data remove karna.

Array middle delete → O(n)
Linked list delete → O(1) (if pointer known)

### ⭐ (4) Searching

* Linear search → O(n)
* Binary search → O(log n)

### ⭐ (5) Sorting

Data ko order me lagana.
Bubble sort, selection sort etc.

### ⭐ (6) Updating

Data ki value modify karna.

---

# **2. Algorithm Analysis**

## ⭐ 2.1 Time Complexity (Deep Explanation)**

Time complexity =
**Number of basic operations** performed with respect to input size (n).

### ✔ Why important?

* Compare algorithms
* Predict performance
* Choose best for large input

---

## ⭐ Time Complexity Types

### ✔ Best Case

Minimum time
Ex: Linear search me required element = **first position**

### ✔ Worst Case

Maximum time
Ex: Linear search key = **last position / absent**

### ✔ Average Case

Probability basis par average time

---

## ⭐ 2.2 Space Complexity

Total memory required =
**Input space + Auxiliary space**

Example (VERY IMPORTANT):

* Bubble sort → auxiliary space = O(1)
* Merge sort → auxiliary space = O(n)

---

# ⭐ 2.3 Asymptotic Notations (FULL MARKS HERE)

## **1. Big-O (Upper Bound)**

Worst case time

Notations example:

* O(1) → Constant time
* O(log n) → Binary search
* O(n) → Linear search
* O(n log n) → Merge sort
* O(n²) → Bubble sort
* O(2ⁿ) → Recursion of subset
* O(n!) → Travelling salesman (TSP)

---

## **2. Omega – Ω**

Best case
Ex: Binary search best = Ω(1)

---

## **3. Theta – Θ**

Average = Tight bound
Ex: Linear search average = Θ(n)

---

## ⭐ Order of Growth (VERY IMPORTANT LIST)**

Memorize:

```
1 < log n < n < n log n < n² < n³ < 2ⁿ < n!
```

---

# **3. Searching Techniques**

---

# ⭐ 3.1 Linear Search

### ✔ Concept

Har element ko sequentially check karte hain.

### ✔ Algorithm (Exam-ready)

```
LinearSearch(A, n, key)
1. for i = 0 to n-1
2.     if A[i] == key
3.         return i
4. return -1
```

---

### ✔ Dry Run Diagram

Array: [5,8,12,3]
Key = 12

```
i=0 → 5 ≠ 12  
i=1 → 8 ≠ 12  
i=2 → 12 ✔ FOUND  
```

---

## ⭐ Time Complexity

Best: O(1)
Worst: O(n)
Average: O(n)

---

# ⭐ 3.2 Binary Search (Divide & Conquer)

**Condition: Array must be sorted**

---

### ✔ Algorithm

```
BinarySearch(A, low, high, key)
1. while low ≤ high
2.     mid = (low + high) / 2
3.     if A[mid] == key → return mid
4.     else if key < A[mid] → high = mid - 1
5.     else → low = mid + 1
6. return -1
```

---

### ✔ Trace Table Example

Array = [4,7,9,12,16,20]
Key = 12

| Step | Low | High | Mid | A[mid] | Decision          |
| ---- | --- | ---- | --- | ------ | ----------------- |
| 1    | 0   | 5    | 2   | 9      | key > mid → right |
| 2    | 3   | 5    | 4   | 16     | key < mid → left  |
| 3    | 3   | 3    | 3   | 12     | FOUND             |

---

## ⭐ Time Complexity

Best → O(1)
Worst → **O(log n)**
Average → O(log n)

---

# **4. Linear vs Binary Search (FULL TABLE)**

| Feature      | Linear              | Binary            |
| ------------ | ------------------- | ----------------- |
| Requirement  | Unsorted OK         | Sorted required   |
| Method       | Check each element  | Divide array      |
| Time (Worst) | O(n)                | O(log n)          |
| Performance  | Slow for large data | Very fast         |
| Used when    | Small/unsorted data | Large/sorted data |

---

# ⭐ 5. Solved Questions (EXAM LEVEL)

---

## ✔ **Q1. Define Data Structure. Explain its classification. (5 Marks)**

**Definition + two diagrams + examples**
(Apne notes me included above)

---

## ✔ **Q2. Explain Big-O notation with examples. (5 Marks)**

Important points:

* Upper bound
* Represents worst case
* Example:
  Linear search → O(n)
  Binary search → O(log n)

---

## ✔ **Q3. Write algorithm + dry run of Linear Search. (5 Marks)**

→ Complete algorithm + example table
(Fully provided above)

---

## ✔ **Q4. Binary Search algorithm + trace table. (10 Marks)**

→ Most scoring
(Fully provided above)

---

# ⭐ 6. Mind Maps / Diagrams (ASCII)

### ✔ Data Structure Classification

```
                     DATA STRUCTURE
                   /                \
              Linear               Non-Linear
            /    |    \              /    \
         Array List Queue         Tree   Graph
```

---

### ✔ Time Complexity Chart (Memory Trick)

```
FAST → Slow
O(1) < O(log n) < O(n) < O(n log n) < O(n²)
```

---

# ⭐ 7. Extra Important Viva Questions (2–3 Marks)

1. Algorithm kya hota hai?
2. Big-O kyun use hota hai?
3. Linear vs Binary search difference?
4. Time complexity define karo.
5. Traverse ka matlab kya hai?
6. Auxiliary space kya hota hai?

---

# ⭐ 8. Short-Trick Memory Tips

* **Binary search = Half Half Half → LOGICAL → log n**
* **Linear search = Line by line → O(n)**
* **Merge sort → merging arrays → needs extra space → O(n)**
* **Bubble sort → 2 loops → n²**

---
