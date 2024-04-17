# Leet 217. Contains Duplicate

:green_square: Easy

Given an integer array `nums`, return `true` if any value appears at least twice in the array, and return `false` if every element is distinct.

## Examples:

**Example 1:**

Input: `nums = [1,2,3,1]`

Output: `true`

**Example 2:**

Input: `nums = [1,2,3,4]`

Output: `false`

**Example 3:**

Input: `nums = [1,1,1,3,3,4,3,2,4,2]`

Output: `true`

## Constraints:

- `1 <= nums.length <= 10^5`
- `-10^9 <= nums[i] <= 10^9`

## Solution:

```Java
class Solution {
    public boolean containsDuplicate(int[] nums) {
        Set<Integer> set = new HashSet<>();
        for(int num: nums) {
            if(set.contains(num)){
                return true;
            }
            set.add(num);
        }
        return false;
    }
}
```
