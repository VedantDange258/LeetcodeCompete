# 1295. Find Numbers with Even Number of Digits

## 🟢 Difficulty
Easy

## 📖 Problem Statement

Given an array `nums` of integers, return how many of them contain an **even number of digits**.

### Example

**Input**

```text
nums = [12,345,2,6,7896]
```

**Output**

```text
2
```

**Explanation**

- 12 → 2 digits ✅
- 345 → 3 digits ❌
- 2 → 1 digit ❌
- 6 → 1 digit ❌
- 7896 → 4 digits ✅

Therefore, the answer is **2**.

---

## 💡 Approach

1. Initialize a variable `count = 0`.
2. Traverse each number in the array.
3. Convert the number into a string using `str()`.
4. Find the number of digits using `len()`.
5. Check if the number of digits is even using the modulus operator (`%`).
6. If it is even, increment `count`.
7. Return `count`.

---

## 💻 Python Solution

```python
class Solution:
    def findNumbers(self, nums):

        count = 0

        for num in nums:

            digits = len(str(num))

            if digits % 2 == 0:
                count += 1

        return count
```

---

## ⏱ Time Complexity

**O(n)**

- We traverse the array only once.
- Each element is processed one time.

---

## 💾 Space Complexity

**O(1)**

- Only a few extra variables (`count` and `digits`) are used.
- No additional data structure is created.

---

## 📚 Concepts Learned

- Arrays (Lists)
- `for` loop
- `str()` function
- `len()` function
- Modulus operator (`%`)
- Conditional statements (`if`)
- Counting technique

---

## 🚀 What I Learned

- How to count elements based on a condition.
- How to determine the number of digits in an integer.
- Using `str()` and `len()` together.
- Solving array problems using iteration.

---

⭐ Solved as part of my **LeetCode & AI/ML Learning Journey**.
