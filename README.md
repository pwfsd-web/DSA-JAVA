
 Java + DSA Assessment (3 Hours | 100 Marks)

> **PW Skills Java Batch: Final Assessment**
 
# Interview Preparation Test: Java DSA Capstone Grand Assessment

> **PW Java Classes (Java DSA Batch)**
> **Duration:** 3 Hours (180 mins) | **Total Marks:** 100 (MCQ: 40, Coding: 60)

---

## 📌 Candidate Instructions

### Section A: MCQs (Q1 to Q20, 40 Marks)
- Each question carries **2 marks**. **Negative marking: -0.5** for each incorrect answer.
- Submit a **separate document** (PDF / Word / Markdown) named `MCQ_Answers_<YourName>_<RollNo>.pdf`.
- For every question, write your **chosen option (A/B/C/D)** and a **1-2 sentence technical justification**.

### Section B: Coding (Problems 1 to 6, 60 Marks)
- Each problem carries **10 marks**.
- Write clean, production-grade **Java 8+**.
- Submit through **GitHub**: create a public or private repo named `java-dsa-interview-test-<yourname>`.
- Put each solution in its own file (`Problem1.java` ... `Problem6.java`).
- Include a detailed `README.md` explaining your **approach, Time Complexity and Space Complexity** for each problem.
- Submit the repository link on the portal.

### Code Integrity
Brute-force solutions that exceed the time limit (TLE) **will not receive full credit**. Your solution must strictly meet the asymptotic bounds given in each problem.

## 🚀 Suggested Repository Structure

```
java-dsa-interview-test-<yourname>/
├── README.md                  <- approach + complexity for every problem
├── MCQ_Answers_<YourName>_<RollNo>.pdf
└── src/
    ├── Problem1.java          <- Subarray Sum Equals K
    ├── Problem2.java          <- Linked List Cycle II
    ├── Problem3.java          <- Daily Temperatures
    ├── Problem4.java          <- LCA of a Binary Tree
    ├── Problem5.java          <- Course Schedule II
    └── Problem6.java          <- Partition Equal Subset Sum
```

Each file should have a `main` method that runs the sample inputs.

## 🧮 Marks Distribution

| Section | Questions | Marks per Question | Total |
|---|---|---|---|
| A: MCQ | 20 | 2 (-0.5 for wrong) | 40 |
| B: Coding | 6 | 10 | 60 |
| | | **Total** | **100** |


---

# SECTION A: Multiple Choice Questions (20 × 2 = 40 Marks)

Select the single most optimal choice. Submit your answers with reasoning in the MCQ document.

**Q1.** What will be printed to standard output?

```java
String s1 = "Java";
String s2 = new String("Java");
String s3 = s2.intern();
System.out.println((s1 == s2) + " " + (s1 == s3) + " " + s1.equals(s2));
```
- A) `true true true`
- B) `false true true`
- C) `false false true`
- D) `true false true`

---

**Q2.** What is the tightest worst-case time complexity of this recursive function for input `N`?

```java
void solve(int n) {
    if (n <= 1) return;
    for (int i = 1; i <= n; i++) { System.out.print(i); }
    solve(n / 2);
    solve(n / 2);
}
```
- A) O(N)
- B) O(N log N)
- C) O(N²)
- D) O(2^N)

---

**Q3.** For any positive integer `n > 0`, what does `(n & (n - 1)) == 0` evaluate?
- A) Checks if `n` is an odd number
- B) Checks if `n` is a prime number
- C) Checks if `n` is a power of 2
- D) Clears the lowest set bit of `n`

---

**Q4.** Given a sorted array of `N` integers, which technique finds whether a pair with sum `K` exists in **O(N) time and O(1) auxiliary space**?
- A) Binary Search on each element: O(N log N) time, O(1) space
- B) Two Pointers (left at 0, right at N-1) converging inwards: O(N) time, O(1) space
- C) HashSet lookup: O(N) time, O(N) space
- D) Nested loop brute force: O(N²) time, O(1) space

---

**Q5.** To rotate an `N × N` matrix **clockwise by 90°, in place**, which sequence of transformations is required?
- A) Reverse each row, then transpose the matrix
- B) Transpose the matrix, then reverse each row
- C) Transpose the matrix, then reverse each column
- D) Reverse each column, then reverse each row

---

**Q6.** In Java 8 and later, what happens internally when the number of elements in a single `HashMap` bucket exceeds the treeification threshold (`TREEIFY_THRESHOLD = 8`) and total capacity is at least 64?
- A) The bucket immediately throws a `ConcurrentModificationException`
- B) The bucket converts its internal LinkedList into a Red-Black Tree (`TreeNode`), reducing search time from O(N) to O(log N)
- C) The `HashMap` drops colliding keys and retains only the most recent entry
- D) The capacity doubles but the bucket remains an O(N) singly linked list

---

**Q7.** Which sorting algorithm is **stable**, has worst-case time complexity **O(N log N)**, but needs **O(N) auxiliary memory**?
- A) Quick Sort
- B) Heap Sort
- C) Merge Sort
- D) Selection Sort

---

**Q8.** In the "Search on Answer Space" paradigm (e.g. Koko Eating Bananas, Capacity to Ship Packages), what essential property must the feasibility function `canComplete(speed)` satisfy across the search range?
- A) It must be strictly quadratic
- B) It must be monotonic (if speed X is feasible, every speed Y > X is also guaranteed feasible)
- C) It must produce prime values
- D) It must run in O(1) time without reading the input array

---

**Q9.** In Floyd's Cycle Detection Algorithm (Tortoise and Hare), suppose a cycle of length `C` exists. When `slow` enters the cycle, `fast` is already inside. Why are they guaranteed to meet?
- A) Fast moves 2 steps and slow moves 1 step, decreasing the relative gap between them by exactly 1 in every iteration until the gap becomes 0 modulo `C`
- B) Fast reverses direction upon hitting the tail of the list
- C) The call stack forces both pointers to reset to head
- D) Slow accelerates to speed 2 after traversing half the list

---

**Q10.** What is the total amortized time complexity of finding the "Next Greater Element" for all `N` elements using a Monotonic Decreasing Stack?
- A) O(N²) because of the `while` loop inside the `for` loop
- B) O(N log N) because elements are maintained in sorted order
- C) O(N) because every element is pushed onto the stack exactly once and popped at most once
- D) O(1) auxiliary space and O(N) time

---

**Q11.** To solve "Sliding Window Maximum" for an array of size `N` with window size `K` in optimal **O(N)** time, which data structure is used and what invariant is maintained?
- A) Standard FIFO Queue maintaining elements in arrival order
- B) Monotonic Deque (`ArrayDeque`) storing indices with values in strictly decreasing order
- C) Min-Heap of size `K` storing indices
- D) Stack storing the maximum element seen so far

---

**Q12.** If the **Inorder traversal** of a binary tree visits nodes in sorted ascending order, which statement MUST be true?
- A) The tree is a Complete Binary Tree
- B) The tree is a valid Binary Search Tree (BST)
- C) The tree has minimum possible height
- D) The Postorder traversal will also be sorted

---

**Q13.** When deleting a node with **two children** from a BST, what is the standard replacement node to maintain the BST invariant?
- A) The root of the whole tree
- B) Either the Inorder Predecessor (maximum of left subtree) or the Inorder Successor (minimum of right subtree)
- C) The left child's immediate left leaf
- D) Any arbitrary node with 0 children

---

**Q14.** What is the optimal time complexity to find the **K-th largest** element in an unsorted stream of `N` elements using a heap?
- A) O(N log N) by inserting all elements into a Max-Heap
- B) O(N log K) by maintaining a Min-Heap of bounded size `K`
- C) O(K log N) by building an array and using Selection Sort
- D) O(N) space and O(N²) time

---

**Q15.** Why does BFS guarantee the shortest path between two nodes in an **unweighted** graph, whereas DFS does not?
- A) BFS visits nodes radially layer by layer; any path of length `L` is completely evaluated before discovering paths of length `L+1`
- B) BFS uses recursion which minimizes call stack depth
- C) BFS sorts edge weights dynamically using a `PriorityQueue`
- D) DFS cannot handle graphs with cycles even with a visited array

---

**Q16.** Which algorithm is correct for single-source shortest paths in a **directed graph with negative edge weights but no negative-weight cycles**?
- A) Dijkstra's Algorithm using a Min-Heap: O(E log V)
- B) Standard BFS using a Queue: O(V + E)
- C) Bellman-Ford Algorithm: O(V × E)
- D) Prim's Algorithm: O(E log V)

---

**Q17.** In Kahn's Algorithm for Topological Sort on a directed graph with `V` vertices, what indicates the presence of a directed cycle?
- A) The in-degree of all vertices becomes zero immediately
- B) The number of vertices processed from the Queue is strictly less than `V`
- C) The Queue overflows its maximum capacity
- D) The adjacency list contains disconnected components

---

**Q18.** Consider Coin Change with denominations `{1, 3, 4}` and target amount `6`. What do the **Greedy** approach and the optimal **DP** approach produce?
- A) Greedy: 2 coins {3, 3}; DP: 3 coins {4, 1, 1}
- B) Greedy: 3 coins {4, 1, 1}; DP: 2 coins {3, 3}
- C) Both Greedy and DP produce 2 coins {3, 3}
- D) Both Greedy and DP fail because coin change is unsolvable

---

**Q19.** In the Longest Common Subsequence (LCS) problem for strings `S1` (length M) and `S2` (length N), what is the state transition when `S1[i-1] != S2[j-1]`?
- A) `dp[i][j] = 1 + dp[i-1][j-1]`
- B) `dp[i][j] = Math.max(dp[i-1][j], dp[i][j-1])`
- C) `dp[i][j] = Math.min(dp[i-1][j], dp[i][j-1]) + 1`
- D) `dp[i][j] = 0`

---

**Q20.** When generating all subsets of an array with backtracking, what happens if the developer writes `result.add(tempList);` instead of `result.add(new ArrayList<>(tempList));`?
- A) The code throws a `CompileTimeTypeMismatchException`
- B) It creates an infinite recursive loop
- C) The result list ends up containing references to the same mutable list object, which ends up empty `[[], [], ...]` after un-choosing
- D) Java automatically deep-copies the list during `List.add()`

---

# SECTION B: Coding Problems (6 × 10 = 60 Marks)

All solutions must be in **Java 8+**. Include time and space complexity explanations in your repo README.

## Problem 1: Subarray Sum Equals K (10 Marks)

Given an integer array `nums` (may contain **positive and negative** integers) and an integer `k`, return the **total number of continuous subarrays** whose sum equals `k`.

**Mandate:** Your solution must run in **O(N)** time.

**Constraints**
- `1 <= nums.length <= 2 * 10^4`
- `-1000 <= nums[i] <= 1000`
- `-10^7 <= k <= 10^7`
- Expected Time: **O(N)** | Expected Space: **O(N)**

**Example 1**
```
Input : nums = [1, 1, 1], k = 2
Output: 2
Explanation: Subarrays [1, 1] at indices [0, 1] and [1, 2] both sum to 2.
```

**Example 2**
```
Input : nums = [1, 2, 3, -2, 1], k = 3
Output: 3
Explanation: Subarrays [1, 2], [3], and [2, 3, -2] all sum to 3.
```

---

## Problem 2: Linked List Cycle II (10 Marks)

Given the `head` of a singly linked list, return the **node where the cycle begins**. If there is no cycle, return `null`.

A cycle exists if some node can be reached again by continuously following the `next` pointer.

**Mandate:** Solve **without modifying the linked list** and using only **O(1) auxiliary memory**. Solutions using extra collections (like `HashSet`) will not receive full credit.

**Constraints**
- Number of nodes is in the range `[0, 10^4]`
- `-10^5 <= Node.val <= 10^5`
- Expected Time: **O(N)** | Expected Auxiliary Space: **O(1)**

**Example 1**
```
Input : head = [3, 2, 0, -4], pos = 1   (tail connects to the node at index 1)
Output: reference to the Node with value 2
```

**Example 2**
```
Input : head = [1, 2], pos = -1   (no cycle)
Output: null
```

---

## Problem 3: Daily Temperatures (10 Marks)

Given an array `temperatures` of daily temperatures, return an array `answer` where `answer[i]` is the number of days you have to wait after day `i` to get a **warmer** temperature. If no future day is warmer, keep `answer[i] = 0`.

**Mandate:** O(N²) solutions will exceed the time limit (TLE). Achieve optimal **linear** time.

**Constraints**
- `1 <= temperatures.length <= 10^5`
- `30 <= temperatures[i] <= 100`
- Expected Time: **O(N)** | Expected Space: **O(N)**

**Example 1**
```
Input : temperatures = [73, 74, 75, 71, 69, 72, 76, 73]
Output: [1, 1, 4, 2, 1, 1, 0, 0]
Explanation: Day 0 (73): day 1 is warmer (74), wait = 1.
             Day 2 (75): day 6 is warmer (76), wait = 4.
```

**Example 2**
```
Input : temperatures = [30, 40, 50, 60]
Output: [1, 1, 1, 0]
```

---

## Problem 4: Lowest Common Ancestor of a Binary Tree (10 Marks)

Given a binary tree, find the **Lowest Common Ancestor (LCA)** of two given nodes `p` and `q`.

The LCA is the lowest node in the tree that has both `p` and `q` as descendants (**a node can be a descendant of itself**).

**Mandate:** Implement an optimal **recursive** solution that visits each node **at most once**, **without** external parent-pointer maps.

**Constraints**
- Number of nodes is in the range `[2, 10^5]`
- `-10^9 <= Node.val <= 10^9`
- All `Node.val` are unique. `p` and `q` are guaranteed to exist in the tree.
- Expected Time: **O(N)** | Expected Auxiliary Space: **O(H)**, where `H` is the tree height

**Example 1**
```
Input : root = [3, 5, 1, 6, 2, 0, 8, null, null, 7, 4], p = 5, q = 1
Output: 3
Explanation: The LCA of nodes 5 and 1 is 3.
```

**Example 2**
```
Input : root = [3, 5, 1, 6, 2, 0, 8, null, null, 7, 4], p = 5, q = 4
Output: 5
Explanation: The LCA of nodes 5 and 4 is 5, since a node can be a descendant of itself.
```

---

## Problem 5: Course Schedule II (10 Marks)

There are `numCourses` courses labelled `0` to `numCourses - 1`. You are given an array `prerequisites` where `prerequisites[i] = [a_i, b_i]` means you must take course `b_i` **first** to take course `a_i`.

Return an **ordering** of courses to finish all of them. If there are multiple valid orderings, return **any** of them. If it is impossible (dependency deadlock), return an **empty array** `[]`.

**Mandate:** Detect dependency cycles and output a valid order in **linear time**.

**Constraints**
- `1 <= numCourses <= 2000`
- `0 <= prerequisites.length <= numCourses * (numCourses - 1)`
- `prerequisites[i].length == 2`
- Expected Time: **O(V + E)** | Expected Space: **O(V + E)**

**Example 1**
```
Input : numCourses = 2, prerequisites = [[1, 0]]
Output: [0, 1]
```

**Example 2**
```
Input : numCourses = 4, prerequisites = [[1,0], [2,0], [3,1], [3,2]]
Output: [0, 2, 1, 3]   (or [0, 1, 2, 3])
```

**Example 3**
```
Input : numCourses = 2, prerequisites = [[1,0], [0,1]]
Output: []
Explanation: A cycle exists between 0 and 1.
```

---

## Problem 6: Partition Equal Subset Sum (10 Marks)

Given an integer array `nums`, return `true` if you can partition it into **two subsets with equal sum**, otherwise `false`.

**Mandate:** Exponential brute force O(2^N) will exceed the time limit. Use optimal **polynomial** time.

**Constraints**
- `1 <= nums.length <= 200`
- `1 <= nums[i] <= 100`
- Expected Time: **O(N × target)**, where `target = sum / 2`
- Expected Space: **O(target)**

**Example 1**
```
Input : nums = [1, 5, 11, 5]
Output: true
Explanation: Partition as [1, 5, 5] and [11], both sum to 11.
```

**Example 2**
```
Input : nums = [1, 2, 3, 5]
Output: false
Explanation: totalSum = 11 (odd), so it cannot be split into two equal integer subsets.
```

---

# 📝 README Template for Your Submission

Copy this into the `README.md` of **your own** repo and fill it in.

```markdown
# Java DSA Interview Test: <Your Name> (<Roll No>)

## Problem 1: Subarray Sum Equals K
**Approach:** <your idea in 2-4 lines>
**Time Complexity:** O(...)  |  **Space Complexity:** O(...)

## Problem 2: Linked List Cycle II
**Approach:**
**Time Complexity:**  |  **Space Complexity:**

## Problem 3: Daily Temperatures
...

## Problem 4: LCA of a Binary Tree
...

## Problem 5: Course Schedule II
...

## Problem 6: Partition Equal Subset Sum
...
```

---

**End of Question Paper. All the best! 🚀**

*Confidential: Evaluated Assessment | Physics Wallah Java DSA*

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
