# 9. Palindrome Number

## Problem

Determine whether a given integer is a palindrome. A palindrome is a number that reads the same forward and backward.

## Approach

Instead of converting the integer into a string, reverse only half of the number.

* Negative numbers cannot be palindromes.
* Numbers ending with `0` (except `0` itself) cannot be palindromes.
* Reverse the last half of the digits while keeping the first half unchanged.
* Compare both halves:

  * For even-length numbers, both halves should be equal.
  * For odd-length numbers, ignore the middle digit before comparison.

This approach satisfies the follow-up requirement of solving the problem without converting the integer to a string.

## Algorithm

1. If the number is negative, return `False`.
2. If the number ends with `0` but is not `0`, return `False`.
3. Initialize `reversed_half` as `0`.
4. Reverse digits until `reversed_half` is greater than or equal to the remaining number.
5. Compare:

   * `x == reversed_half`, or
   * `x == reversed_half // 10` (for odd-digit numbers).

## Python 3 Solution

```python
class Solution:
    def isPalindrome(self, x: int) -> bool:
        if x < 0 or (x % 10 == 0 and x != 0):
            return False

        reversed_half = 0

        while x > reversed_half:
            reversed_half = reversed_half * 10 + x % 10
            x //= 10

        return x == reversed_half or x == reversed_half // 10
```

## Complexity Analysis

* **Time Complexity:** `O(log₁₀ n)`
* **Space Complexity:** `O(1)`

## Key Takeaway

By reversing only half of the digits instead of the entire number, the solution is more efficient, uses constant extra space, and avoids string conversion.
