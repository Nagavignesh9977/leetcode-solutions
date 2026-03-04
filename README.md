# LeetCode Solutions – Java

This repository contains my solutions to LeetCode problems implemented in **Java**.
The goal of this repository is to strengthen my **Data Structures and Algorithms (DSA)** knowledge and improve **problem-solving skills** through consistent practice.

I am currently focusing on topics such as **Binary Search, Arrays, Matrix operations, and algorithm optimization**.

---

## 📚 Problems Solved

| #    | Problem                              | Difficulty | Topic           | Solution |
| ---- | ------------------------------------ | ---------- | --------------- | -------- |
| 875  | Koko Eating Bananas                  | Medium     | Binary Search   | Java     |
| 1582 | Special Positions in a Binary Matrix | Easy       | Matrix / Arrays | Java     |

---

# 1️⃣ LeetCode 875 – Koko Eating Bananas

### 📌 Problem Summary

Koko loves eating bananas. There are several piles of bananas, and each pile has a certain number of bananas.
Koko can decide her **eating speed (k bananas per hour)**.

Each hour:

* Koko chooses a pile
* Eats **k bananas from that pile**
* If the pile has fewer than k bananas, she eats all of them

The goal is to **find the minimum integer k such that Koko can eat all bananas within h hours**.

---

### 💡 Approach

This problem can be efficiently solved using **Binary Search**.

Instead of checking every possible speed from `1 → max(pile)`, we apply binary search to find the **minimum feasible eating speed**.

Steps:

1. Set search range:

   * `low = 1`
   * `high = maximum pile size`

2. Use binary search to find the minimum speed.

3. For each speed `mid`:

   * Calculate total hours required:

   ```
   hours += ceil(pile / mid)
   ```

4. If total hours ≤ `h`
   → This speed is possible, try smaller speed.

5. If total hours > `h`
   → Speed is too slow, increase speed.

---

### ⏱ Time Complexity

```
O(n log m)
```

Where:

* `n` = number of piles
* `m` = maximum bananas in a pile

---

### 💾 Space Complexity

```
O(1)
```

---

# 2️⃣ LeetCode 1582 – Special Positions in a Binary Matrix

### 📌 Problem Summary

You are given an **m × n binary matrix**.

A position `(i, j)` is called **special** if:

* `mat[i][j] == 1`
* All other elements in **row i** are `0`
* All other elements in **column j** are `0`

Your task is to **count the number of special positions** in the matrix.

---

### 💡 Approach

To solve this efficiently:

1. Count number of `1s` in each row.
2. Count number of `1s` in each column.
3. Traverse the matrix again.
4. A position is special if:

```
mat[i][j] == 1
AND
rowCount[i] == 1
AND
colCount[j] == 1
```

---

### ⏱ Time Complexity

```
O(m × n)
```

---

### 💾 Space Complexity

```
O(m + n)
```

---

# 🧠 Topics Covered

* Binary Search
* Matrix Traversal
* Arrays
* Optimization Techniques

---

# 🎯 Learning Goal

This repository is part of my continuous effort to:

* Strengthen **DSA fundamentals**
* Improve **algorithmic thinking**
* Prepare for **technical interviews**
* Build a consistent **problem-solving habit**

---

# 💻 Language Used

* **Java**

---

# 🚀 Future Plan

I will continue solving problems from:

* Arrays
* Binary Search
* Strings
* Dynamic Programming
* Graphs
* Trees

---

# 👨‍💻 Author

**Anumula Nagavignesh**

Data Scientist | Machine Learning Enthusiast
Skilled in **Python, SQL, Machine Learning, and Data Analytics**

GitHub:
https://github.com/Nagavignesh9977

LeetCode:
https://leetcode.com/Vigneshnaga2005

---
