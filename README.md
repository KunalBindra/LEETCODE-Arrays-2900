# LEETCODE-Arrays-2900
---

### 🔍 Problem Statement

Given:

* An array of words `words[]`
* An array of integers `groups[]` (same length as `words[]`)

Each `groups[i]` represents the group number of `words[i]`.
Your task is to return the **longest subsequence of words** such that **no two consecutive words** come from the **same group**.

---
---

### 🧠 How It Works (Step-by-step)

1. **Initialize** an empty list `ans` to store the result.
2. Use a variable `gd` (group detected) to keep track of the previous group seen. Start with `-1`.
3. Loop through all elements in `groups[]`:

   * If the current group is different from `gd`, add the word to the answer.
   * Update `gd` to the current group.
4. Return the final list of selected words.

---

### 🧪 Example

```java
String[] words = {"a", "b", "c", "d", "e"};
int[] groups = {1, 1, 2, 2, 3};
```

**Output:** `["a", "c", "e"]`

**Why?**

* Start with "a" from group 1 ✅
* Skip "b" (same group as "a") ❌
* "c" is from group 2 ✅
* Skip "d" (same group as "c") ❌
* "e" is from group 3 ✅

---

### 💡 Summary

* Picks the **first word** from each **new group**.
* Ensures **no two selected words** are from the **same group** consecutively.

---
