 Java + DSA Assessment (3 Hours | 100 Marks)

> **PW Skills Java Batch: Final Assessment**
 

---

## 📌 Instructions

- **Duration:** 3 hours (180 minutes)
- **Language:** Java only
- **Attempt all questions.** Marks are shown against each question.
- Write **time and space complexity** as a comment above every solution. Each coding problem carries 20% of its marks for this.
- Handle **edge cases**: empty input, negatives, duplicates, overflow.
- No internet, no AI tools, no copying from classmates. You may use your own notes and the class resources.
- Do **not** use built-in shortcuts when the question says not to (for example `Integer.toBinaryString`).

## 🚀 How to Submit (on GitHub)

1. **Fork** this repository (or create a new repo named `java-assessment-<yourname>`).
2. Clone it and create the folder structure below.
3. Solve each question in its own file. Commit after each question, for example `git commit -m "Solved Q5"`.
4. Push to your repo before time ends and submit the repo link.

```
src/
├── sectionA/   Q1.java  Q2.java  Q3.java  Q4.java
├── sectionB/   Q5.java  Q6.java  Q7.java
├── sectionC/   Q8_Library/ (multiple files)  Q9.java  Q10.java
├── sectionD/   Q11.java Q12.java Q13.java Q14.java Q15.java
└── sectionE/   Q16.java Q17.java Q18.java
```

Each file should have a `main` method that **tests your solution with the sample inputs**.

## 🧮 Marking Scheme

| Criteria | Weight |
|---|---|
| Correct logic and output | 60% |
| Edge cases handled | 20% |
| Time and space complexity stated correctly | 20% |

| Section | Topics | Marks | Suggested Time |
|---|---|---|---|
| A | Basics, Type Casting, Bits | 20 | 25 min |
| B | Arrays, Strings, Functions | 20 | 30 min |
| C | OOP, Recursion, HashMap/HashSet | 20 | 35 min |
| D | Two Pointers, Sorting, Binary Search, Linked List, Stack/Queue, Trees | 25 | 50 min |
| E | Heap, Graphs, DP/Greedy/Backtracking | 15 | 40 min |
| | **Total** | **100** | **180 min** |

 
---

# Section A: Fundamentals (20 Marks)

### Q1. Predict the Output (5 Marks)
Write the output of the code below **and explain why** in a comment (type casting, overflow, increment operators, char arithmetic).

```java
public class Q1 {
    public static void main(String[] args) {
        int a = 10;
        byte b = (byte) 130;
        char c = 'A';

        System.out.println(a++ + ++a);
        System.out.println(b);
        System.out.println(c + 1);
        System.out.println((char) (c + 1));
        System.out.println(10 / 4 + 10 % 4 + 10 / 4.0);
    }
}
```

---

### Q2. Digits and Powers (5 Marks)

**(a)** Given a 4-digit number `n`, split its digits into **two new numbers** so that their sum is **minimum**. Return that sum.

```
Input : 2932      Output: 52     (split into 23 and 29)
Input : 4009      Output: 13     (split into 04 and 09)
```

**(b)** Write `isPowerOfTwo(int n)` and `isPowerOfFour(int n)` **without loops or recursion** (use bit manipulation).

```
isPowerOfTwo(16)  -> true      isPowerOfFour(16) -> true
isPowerOfTwo(8)   -> true      isPowerOfFour(8)  -> false
isPowerOfTwo(0)   -> false
```

---

### Q3. Bit Manipulation (5 Marks)

**(a)** Count the number of **set bits** (1s) in an integer `n`.
```
Input: 13 (1101)   Output: 3
```

**(b)** **Swap two numbers without a temp variable** (and without `+`/`-` if you can).
```
a = 5, b = 9   ->   a = 9, b = 5
```

**(c)** Every element in the array appears twice except one. **Find the single element** in O(n) time and O(1) space.
```
Input : [4, 1, 2, 1, 2]    Output: 4
```

---

### Q4. Number System (5 Marks)

Without using `Integer.toBinaryString` or `Integer.parseInt(s, 2)`:

**(a)** Convert a decimal number to a binary string.
```
Input: 10    Output: "1010"
```

**(b)** Convert a binary string to a decimal number.
```
Input: "1101"    Output: 13
```

---

# Section B: Arrays, Strings, Functions (20 Marks)

### Q5. Matrix (8 Marks)

Given an `n × n` matrix:

**(a)** **Rotate it 90° clockwise in place** (no extra matrix).
**(b)** **Print it in spiral order.**

```
Input:
1  2  3
4  5  6
7  8  9

(a) After rotation:
7  4  1
8  5  2
9  6  3

(b) Spiral order of the original: 1 2 3 6 9 8 7 4 5
```

---

### Q6. Strings (6 Marks)

**(a)** Check whether a string is a **valid palindrome**, ignoring non-alphanumeric characters and case.
```
Input: "A man, a plan, a canal: Panama"    Output: true
Input: "race a car"                        Output: false
```

**(b)** Return the **longest palindromic substring** (expand around centre, O(n²)).
```
Input: "babad"    Output: "bab" (or "aba")
Input: "cbbd"     Output: "bb"
```

---

### Q7. Arrays (6 Marks)

**(a)** **Move all zeroes to the end** while keeping the order of the other elements (in place).
```
Input : [0, 1, 0, 3, 12]    Output: [1, 3, 12, 0, 0]
```

**(b)** Find the **maximum subarray sum** (Kadane's algorithm).
```
Input : [-2, 1, -3, 4, -1, 2, 1, -5, 4]    Output: 6    (subarray [4, -1, 2, 1])
```

---

# Section C: OOP, Recursion, Collections (20 Marks)

### Q8. Library Management System: OOP Design (8 Marks)

Build a small console program using proper OOP:

| Requirement | Details |
|---|---|
| Abstract class `Item` | Fields: `id`, `title`. Abstract method `double calculateFine(int daysLate)` |
| `Book` extends `Item` | Fine = ₹2 per day |
| `Magazine` extends `Item` | Fine = ₹1 per day, maximum ₹30 |
| Interface `Borrowable` | Methods: `borrow()` and `returnItem()` |
| Concepts to show | Encapsulation (private fields + getters/setters), constructors, method overriding, **polymorphism** |

In `main`: create an `ArrayList<Item>` with at least 2 books and 2 magazines, then loop over it and print each item's fine for `daysLate = 20`.

**Expected output (sample):**
```
Book: Java Basics   | Fine: 40.0
Magazine: Tech Today | Fine: 20.0
```

---

### Q9. Recursion (6 Marks)

**(a)** Print **all subsets** of an array.
```
Input: [1, 2, 3]
Output: [], [1], [2], [3], [1,2], [1,3], [2,3], [1,2,3]   (any order)
```

**(b)** Check whether an array is **sorted** (ascending) using recursion.
```
[1, 2, 3, 4] -> true      [1, 3, 2] -> false
```

**(c)** **Tower of Hanoi**: print every move for `n` discs from rod `A` to rod `C` using rod `B`.
```
n = 2:
Move disc 1 from A to B
Move disc 2 from A to C
Move disc 1 from B to C
```

---

### Q10. HashMap / HashSet (6 Marks)

**(a)** **Two Sum:** return the indices of the two numbers that add up to `target`.
```
Input : nums = [2, 7, 11, 15], target = 9    Output: [0, 1]
```

**(b)** Return the **first non-repeating character** in a string (or `-1` if none).
```
Input: "leetcode"    Output: 'l'
Input: "aabb"        Output: -1
```

**(c)** **Group Anagrams.**
```
Input : ["eat", "tea", "tan", "ate", "nat", "bat"]
Output: [["eat","tea","ate"], ["tan","nat"], ["bat"]]
```

---

# Section D: Core DSA (25 Marks)

### Q11. Two Pointers / Sliding Window (6 Marks)

**(a)** Length of the **longest substring without repeating characters**.
```
Input: "abcabcbb"    Output: 3     ("abc")
Input: "bbbbb"       Output: 1
```

**(b)** **Minimum size subarray** whose sum is **≥ target** (return 0 if none).
```
Input : target = 7, nums = [2, 3, 1, 2, 4, 3]    Output: 2    ([4, 3])
```

---

### Q12. Sorting and Binary Search (5 Marks)

**(a)** Implement **Merge Sort**.
```
Input: [38, 27, 43, 3, 9, 82, 10]    Output: [3, 9, 10, 27, 38, 43, 82]
```

**(b)** Search for `target` in a **rotated sorted array** in **O(log n)**. Return the index or `-1`.
```
Input : nums = [4, 5, 6, 7, 0, 1, 2], target = 0    Output: 4
Input : nums = [4, 5, 6, 7, 0, 1, 2], target = 3    Output: -1
```

---

### Q13. Linked List (6 Marks)

Use this node class:
```java
class ListNode {
    int val;
    ListNode next;
    ListNode(int val) { this.val = val; }
}
```

**(a)** **Detect a cycle** in a singly linked list and **remove it**. Return the head.
```
Input : 1 -> 2 -> 3 -> 4 -> 5 -> (back to 3)
Output: 1 -> 2 -> 3 -> 4 -> 5 -> null
```

**(b)** **Reverse nodes in groups of k.** Leftover nodes (fewer than k) stay as they are.
```
Input : 1 -> 2 -> 3 -> 4 -> 5, k = 2    Output: 2 -> 1 -> 4 -> 3 -> 5
Input : 1 -> 2 -> 3 -> 4 -> 5, k = 3    Output: 3 -> 2 -> 1 -> 4 -> 5
```

---

### Q14. Stack and Queue (4 Marks)

**(a)** Implement a **Queue using two Stacks** with `push(x)`, `pop()`, `peek()` and `empty()`.

**(b)** **Next Greater Element:** for each element, find the next greater element to its right (`-1` if none). Use a monotonic stack, O(n).
```
Input : [4, 5, 2, 25]    Output: [5, 25, 25, -1]
```

---

### Q15. Binary Tree / BST (4 Marks)

Use this node class:
```java
class TreeNode {
    int val;
    TreeNode left, right;
    TreeNode(int val) { this.val = val; }
}
```

**(a)** Check whether a binary tree is a **valid BST**.
```
    5                 5
   / \               / \
  1   7     ->  true 1   4    -> false
     / \                / \
    6   8              3   6
```

**(b)** Find the **Lowest Common Ancestor (LCA)** of two nodes `p` and `q` in a binary tree.
```
Tree: [3,5,1,6,2,0,8]    p = 5, q = 1    Output: 3
Tree: [3,5,1,6,2,0,8]    p = 5, q = 4 (child of 2)  -> LCA = 5
```

---

# Section E: Advanced DSA (15 Marks)

### Q16. Heap / Priority Queue (5 Marks)

**(a)** Find the **K-th largest element** in an array (use a min-heap of size k).
```
Input : nums = [3, 2, 1, 5, 6, 4], k = 2    Output: 5
```

**(b)** **Merge K sorted arrays** into one sorted array using a min-heap.
```
Input : [[1, 4, 5], [1, 3, 4], [2, 6]]
Output: [1, 1, 2, 3, 4, 4, 5, 6]
```

---

### Q17. Graphs (5 Marks)

**(a)** **Number of Islands:** given a grid of `'1'` (land) and `'0'` (water), count the islands (DFS or BFS).
```
Input:
1 1 0 0 0
1 1 0 0 0
0 0 1 0 0
0 0 0 1 1

Output: 3
```

**(b)** **Course Schedule:** there are `n` courses (`0` to `n-1`). `prerequisites[i] = [a, b]` means you must take `b` before `a`. Return `true` if all courses can be finished.
```
Input : n = 2, prerequisites = [[1, 0]]           Output: true
Input : n = 2, prerequisites = [[1, 0], [0, 1]]   Output: false
```

---

### Q18. DP / Greedy / Backtracking: Choose ONE (5 Marks)

Solve **any one** of these completely:

**Option 1: 0/1 Knapsack (DP)**
```
Input : weights = [1, 3, 4, 5], values = [1, 4, 5, 7], capacity = 7
Output: 9      (take items with weights 3 and 4)
```

**Option 2: Minimum Number of Platforms (Greedy)**
```
Input : arr = [900, 940, 950, 1100, 1500, 1800]
        dep = [910, 1200, 1120, 1130, 1900, 2000]
Output: 3
```

**Option 3: N-Queens (Backtracking)**
```
Input : n = 4
Output: 2 distinct solutions, print each board with 'Q' and '.'
```

---

## 🏁 Before You Submit

- [ ] Every file compiles and runs
- [ ] Complexity written as a comment in every solution
- [ ] Edge cases tested (empty array, single element, negatives)
- [ ] All questions committed and pushed to GitHub
- [ ] Repo link submitted

**All the best! 🚀**

# DSA-JAVA
