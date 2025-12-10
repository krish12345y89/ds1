
# 🟦 **UNIT–3: LINKED LISTS (FULL NOTES)**

---

# ⭐ **1. Introduction to Linked List**

Linked List ek **linear data structure** hai jisme elements **nodes** ki form me store hote hain.

Har **node** me do parts hote hain:

1. **Data**
2. **Pointer** (next node ka address)

Nodes memory me **contiguous** (saath-saath) nahi hote — isliye Linked List **dynamic memory** use karti hai.

---

# ⭐ **2. Singly Linked List (SLL)**

### ✔ Structure of Node

```
struct node {
    int data;
    struct node* next;
};
```

### ✔ Features

* One-way traversal
* Dynamic size
* Insertion/Deletion fast
* Random access possible nahi

---

# ⭐ **3. Representation in Memory**

SLL ke nodes **heap memory** me scattered hote hain.
Har node apne next node ka address store karta hai.

Example diagram:

```
[10 | *] --> [20 | *] --> [30 | *] --> NULL
```

---

# ⭐ **4. Basic Operations on SLL**

---

## 🔵 **4.1 Traversal**

List ko start se end tak access karna.

**Algorithm (Simple):**

1. ptr = head
2. jab tak ptr != NULL
   → print ptr→data
   → ptr = ptr→next

**Time Complexity:** O(n)

---

## 🔵 **4.2 Searching**

Element find karna.

**Worst Case:** Element last me ho → O(n)

---

# ⭐ **5. Insertion in SLL**

---

## 🔵 **5.1 Insert at Beginning**

**Steps:**

1. Naya node banao
2. node→next = head
3. head = node

**Complexity:** O(1)

---

## 🔵 **5.2 Insert at End**

**Steps:**

1. Traverse till last
2. last→next = new node
3. new node→next = NULL

**Complexity:** O(n)

---

## 🔵 **5.3 Insert at Specific Position**

**Steps:**

1. Position-1 tak traverse
2. new node→next = current→next
3. current→next = new node

**Complexity:** O(n)

---

# ⭐ **6. Deletion in SLL**

---

## 🔵 **6.1 Delete from Beginning**

**Steps:**

1. temp = head
2. head = head→next
3. free(temp)

**Complexity:** O(1)

---

## 🔵 **6.2 Delete from End**

**Steps:**

1. Last se ek pehle tak traverse
2. free(last)
3. second-last→next = NULL

**Complexity:** O(n)

---

## 🔵 **6.3 Delete from Specific Position**

**Steps:**

1. Position-1 tak traverse
2. temp = current→next
3. current→next = temp→next
4. free(temp)

**Complexity:** O(n)

---

# ⭐ **7. Header Linked List**

Header node = Ek **dummy node** jo actual data store nahi karta.

```
[HEADER] → [10] → [20] → [30]
```

### ✔ Use:

* Insert/delete operations simplified
* Empty list ko handle karna easy

---

# ⭐ **8. Doubly Linked List (DLL)**

### ✔ Node Structure:

```
[prev | data | next]
```

### ✔ Features:

* Two-way traversal
* More memory required
* Insert/delete faster at both ends

---

## 🔵 DLL Operations (Short Notes)

### **Insert at beginning:**

```
new->next = head
head->prev = new
head = new
```

### **Delete a node:**

```
node->prev->next = node->next
node->next->prev = node->prev
free(node)
```

### Time Complexity:

* Best: O(1)
* Search: O(n)

---

# ⭐ **9. Circular Linked List (CLL)**

### ✔ In CLL:

Last node ka next pointer head ko point karta hai:

```
[10] → [20] → [30] → back to [10]
```

---

## 🔵 Operations

### **Insert at End:**

1. new node banao
2. new→next = head
3. last→next = new

### **Delete from Beginning:**

1. last node find karo
2. head = head→next
3. last→next = head

### Complexity:

* Search: O(n)
* Insert start: O(1)
* Insert end: O(n) (unless tail pointer ho to O(1))

---

# ⭐ **10. Advantages of Linked List**

* Dynamic size
* Insertion/deletion easy
* No memory wastage

---

# ⭐ **11. Disadvantages**

* Extra memory for pointer
* Random access nahi
* Reverse traversal only DLL me possible

---

# ⭐ **12. Real Life Applications**

* Music playlist
* Browser back/forward
* OS process scheduling
* Hash chaining

---

# ⭐ **13. Important Exam Questions**

### **Q1. Create, insert, delete & traverse in SLL.**

Answer: Define node → explain operations → write algorithm → draw diagram.

### **Q2. Compare SLL, DLL and CLL.**

Give table (direction, memory, complexity).

### **Q3. Write algorithm for insert at beginning in DLL.**

### **Q4. Why linked list is better than array?**

### **Q5. Draw memory representation of linked list.**

---
