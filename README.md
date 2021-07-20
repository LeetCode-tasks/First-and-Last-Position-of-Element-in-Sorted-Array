# First-and-Last-Position-of-Element-in-Sorted-Array

Given an array of integers `nums` sorted in ascending order, find the starting and ending position of a given target value.

If target is not found in the array, return `[-1, -1]`.

You must write an algorithm with `O(log n)` runtime complexity.

_Example 1:_

Input: `nums = [5,7,7,8,8,10], target = 8`

Output: `[3,4]`


_Example 2:_

Input: `nums = [5,7,7,8,8,10], target = 6`

Output: `[-1,-1]`

_Example 3:_

Input: `nums = [], target = 0`

Output: `[-1,-1]`

### _Constraints:_

`0 <= nums.length <= 10^5`

`-10^9 <= nums[i] <= 10^9`

`nums` is a non-decreasing array.

## Solution in JavaScript
```
var searchRange = function(nums, target) {
    let i = 0, j = nums.length - 1, firstIndex = -1, lastIndex = -1;
    while (i < nums.length) {
            if (nums[i] === target) {
                firstIndex = i
                break
            }
            i++
    }
    
    while (j >= 0) {
        if (nums[j] === target) {
            lastIndex = j
            break
        }
        j--
    }
    
    return [firstIndex, lastIndex]
};
```

`-10^9 <= target <= 10^9`
