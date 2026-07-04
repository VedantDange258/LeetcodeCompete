
<h1 align="center">1480. Running Sum of 1d Array</h1>

## 📝 Problem Statement

Given an array `nums`, return the running sum of the array.

The running sum of an array is defined as:

```text
runningSum[i] = nums[0] + nums[1] + ... + nums[i]
```

---

## 💡 Approach

1. Create an empty list `ans` to store the running sum.
2. Initialize a variable `total` with `0`.
3. Traverse each element in `nums`.
4. Add the current element to `total`.
5. Append `total` to `ans`.
6. Return the `ans` list.

---

## 🚀 Solution (Python)

```python
class Solution:
    def runningSum(self, nums):
        ans = []
        total = 0

        for num in nums:
            total = total + num
            ans.append(total)

        return ans
```

---

## ⏱️ Time Complexity

- **O(n)**

The array is traversed only once.

---

## 💾 Space Complexity

- **O(n)**

An additional list `ans` is used to store the running sums.

---

## 📚 Concepts Used

- Lists
- For Loop
- Variables
- Running Sum
- Array Traversal

---

## ✅ Example

**Input**

```text
nums = [1,2,3,4]
```

**Output**

```text
[1,3,6,10]
```

**Explanation**

```text
1
1 + 2 = 3
1 + 2 + 3 = 6
1 + 2 + 3 + 4 = 10
```
