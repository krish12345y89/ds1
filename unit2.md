✔ ADT Stack
✔ Stack operations + algorithms + complexity
✔ Expression conversion & evaluation
✔ ADT Queue
✔ Types of queues (Simple, Circular, Priority)
✔ Operations + algorithms + complexity

Yeh **Unit 2 FULL LENGTH** notes honge (10 marker + 5 marker + viva + diagrams + examples).
Chalo start karte hain 👇👇

---

# ⭐ **UNIT 2 – STACKS AND QUEUES (EXTREME DEPTH NOTES)**

B.Tech (RAI) – PCC-RAI-303/21
**Full exam-ready version**

---

# 🔶 **1. STACK (Very-very important for exams)**

Stack = **LIFO (Last In First Out)**

### Real Life Examples:

* Plate stack
* Browser back button
* Undo/Redo

---

# ⭐ **1.1 ADT Stack Definition (5 Marker)**

**ADT (Abstract Data Type)** matlab:
→ Sirf *kya* operations honge, aur *kaise* behave karenge — implementation hide hoti hai.

### **Operations in ADT Stack**

1. **push(x)** → insert element
2. **pop()** → delete + return top element
3. **peek() / top()** → only access top element
4. **isEmpty()**
5. **isFull()**
6. **size()**

---

# ⭐ **1.2 Stack Representation**

### **(A) Using Array**

Diagram:

```
Index: 0  1  2  3  4
Stack: 10 20 30 40 --
Top = 3
```

### **(B) Using Linked List**

Diagram:

```
Top → [50 | *] → [40 | *] → [30 | *] → NULL
```

---

# ⭐ **1.3 Stack Algorithms + Complexity**

## ✔ Algorithm: PUSH (Array implementation)

```
Push(S, x)
1. if top == MAX-1
2.      print "Overflow"
3. else
4.      top = top + 1
5.      S[top] = x
```

### Time Complexity: **O(1)**

---

## ✔ Algorithm: POP

```
Pop(S)
1. if top == -1
2.      print "Underflow"
3. else
4.      x = S[top]
5.      top = top - 1
6.      return x
```

### Time Complexity: **O(1)**

---

# ⭐ **1.4 Stack Applications (EXAM-FAVOURITE)**

1. **Expression conversion**

   * Infix → Postfix
   * Infix → Prefix

2. **Expression evaluation**

   * Postfix evaluation
   * Prefix evaluation

3. Recursion

4. Backtracking

5. Parenthesis checking

6. Function call stack

---

# ⭐ **1.5 Expression Conversion (Super Important)**

## 🔥 **1. Infix → Postfix (Shunting Yard Logic)**

Example:

```
A + B * C
```

Steps:

* Operators ke liye stack
* Operands direct output me
* Precedence follow karo:
  (*, /) > (+, -)

Working:

| Symbol | Stack | Output |
| ------ | ----- | ------ |
| A      | -     | A      |
| +      | +     | A      |
| B      | +     | AB     |
| *      | + *   | AB     |
| C      | + *   | ABC    |
| End    | +*    | ABC*+  |

**Final Postfix = ABC*+**

---

## ⭐ **2. Postfix Evaluation Algorithm**

Algorithm:

```
For each symbol:
    if operand → push
    if operator → pop two, apply, push result
```

Example:

```
Postfix: 23*54*+
```

Working:

* 2 3 * → 6
* 5 4 * → 20
* 6 + 20 → 26

**Answer = 26**

---

# 🔷 **2. QUEUE (FIFO – First In First Out)**

Queue → yaad rakho “line me khade log”.

### Real life:

* Ticket counter line
* Printer queue
* CPU scheduling

---

# ⭐ **2.1 ADT Queue Operations**

1. enqueue(x)
2. dequeue()
3. front()
4. rear()
5. isEmpty()
6. isFull()

---

# ⭐ **2.2 Queue Representation**

## ✔ (A) Array Representation (Simple Queue)

```
Front → 0
Rear → 4

Index: 0 1 2 3 4
Value: 10 20 30 40 50
```

But problem: **Wastage of space after dequeue**
Hence → circular queue.

---

# ⭐ **2.3 Simple Queue Algorithms**

## Enqueue:

```
if rear == MAX-1 → overflow
else
    rear++
    Q[rear] = x
```

## Dequeue:

```
if front > rear → underflow
else
    x = Q[front]
    front++
```

**Complexity: O(1)**

---

# ⭐ **2.4 Circular Queue (Most important)**

Circular queue remove space wastage:

```
Index: 0 1 2 3 4   (rear wraps around)
```

Formula:

```
rear = (rear + 1) % MAX
front = (front + 1) % MAX
```

### Condition for FULL:

```
(front == (rear + 1) % MAX)
```

### Condition for EMPTY:

```
front == -1
```

---

# ⭐ **2.5 Priority Queue (Advanced topic)**

### Mathematically:

Each element = (value, priority)

Dequeue → **highest priority** element.

Can be:

* Ascending priority
* Descending priority
* Min priority queue
* Max priority queue

Implementations:

* Array
* Linked list
* Heap (**best**)

---

# 🔥 **3. Types of Queues – Summary Table**

| Type                       | Meaning                  | Use-case        |
| -------------------------- | ------------------------ | --------------- |
| Simple Queue               | FIFO                     | Ticket counter  |
| Circular Queue             | Circular movement        | OS / CPU buffer |
| Priority Queue             | Highest priority first   | OS scheduling   |
| Double Ended Queue (Deque) | Insert/delete both sides | Sliding window  |

---

# ⭐ **4. Queue Algorithms Complexity**

| Operation  | Simple | Circular |
| ---------- | ------ | -------- |
| Enqueue    | O(1)   | O(1)     |
| Dequeue    | O(1)   | O(1)     |
| Front/Rear | O(1)   | O(1)     |

---

# 🔥 **5. Solved Examination Problems**

---

## ✔ Q1. Write algorithms for push & pop operations. (5 Marks)

(Already given above)

---

## ✔ Q2. Convert infix to postfix:

**A + B * (C - D) / E**

Steps:
Postfix =

```
ABCD-*E/+
```

---

## ✔ Q3. Evaluate postfix expression:

**52+83-*4/**

Solution step-by-step:

* 5 2 + → 7
* 8 3 - → 5
* 7 5 * → 35
* 35 4 / → 8.75

**Ans = 8.75**

---

## ✔ Q4. Explain circular queue with overflow and underflow conditions. (5 Marks)

Overflow:

```
(front == (rear + 1) % MAX)
```

Underflow:

```
front == -1
```

---

## ✔ Q5. Difference: Stack vs Queue (3 Marks)

| Stack                | Queue                  |
| -------------------- | ---------------------- |
| LIFO                 | FIFO                   |
| push/pop             | enqueue/dequeue        |
| Example: back button | Example: printer queue |

---

# 🔥 COMPLETE UNIT–2 SUMMARY (Last-minute revision)

* Stack = LIFO
* Queue = FIFO
* Stack applications: conversion, evaluation, recursion
* Queue types: simple, circular, priority
* Circular queue formula:

  ```
  rear = (rear + 1) % MAX
  ```
* Times: all O(1)

---
