
	# 1929. Concatenation of Array

## Problem

Given an integer array `nums`, create a new array `ans` by concatenating `nums` with itself and return `ans`.

### Example

**Input**

```text
nums = [1,2,1]
```

**Output**

```text
[1,2,1,1,2,1]
```

## Solution

```python
class Solution:
    def getConcatenation(self, nums):

        ans = []

        for i in nums:
            ans.append(i)

        for i in nums:
            ans.append(i)

        return ans
```

## Explanation

1. Create an empty list `ans`.
2. Traverse the input list `nums` and append each element to `ans`.
3. Traverse `nums` again and append each element once more.
4. Return the final concatenated list.

## Time Complexity

* **O(n)**

The array is traversed twice, where `n` is the number of elements.

## Space Complexity

* **O(n)**

A new list is created to store the concatenated array.
