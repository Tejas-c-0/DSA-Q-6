# Plus One

## Problem
Given an array of digits representing a number, add 1 to the number and return the result.

---

## Approach
- Traverse the array from the end
- If digit < 9 → add 1 and return
- If digit = 9 → make it 0 and continue (carry)
- If all digits are 9 → add 1 at the front

---

## Complexity
- Time: O(n)
- Space: O(1)

---

## Key Insight
We simulate manual addition from right to left, handling carry for digits equal to 9.

---

## Example
Input: [1,2,9]  
Output: [1,3,0]  

Input: [9,9]  
Output: [1,0,0]

---

## Code
```python
def plusOne(digits):
    for i in range(len(digits) - 1, -1, -1):
        if digits[i] < 9:
            digits[i] += 1
            return digits
        digits[i] = 0

    return [1] + digits
