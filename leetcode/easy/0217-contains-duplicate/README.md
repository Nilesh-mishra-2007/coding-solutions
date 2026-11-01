# Contains Duplicate

![Difficulty](https://img.shields.io/badge/Difficulty-Easy-green)

## Problem

Yahoo
Netflix
Capgemini
Airbnb
Bloomberg

Given an integer array `nums`, return `true` if any value appears  **at least twice**  in the array, and return `false` if every element is distinct.

 

 **Example 1:** 

 **Input:**  nums = [1,2,3,1]

 **Output:**  true

 **Explanation:** 

The element 1 occurs at the indices 0 and 3.

 **Example 2:** 

 **Input:**  nums = [1,2,3,4]

 **Output:**  false

 **Explanation:** 

All elements are distinct.

 **Example 3:** 

 **Input:**  nums = [1,1,1,3,3,4,3,2,4,2]

 **Output:**  true

 

 **Constraints:** 

- 1 <= nums.length <= 105
- -109 <= nums[i] <= 109

## Solution

**Language:** C++  
**Runtime:** 83 ms (beats 30.11%)  
**Memory:** 113 MB (beats 23.63%)  
**Submitted:** 2026-11-01T12:53:12.874Z  

```cpp

class Solution {
public:
    bool containsDuplicate(vector<int>& nums) {
        unordered_set<int> s;

        for (int num : nums) {
            if (s.find(num) != s.end()) {
                return true;
            }
            s.insert(num);
        }

        return false;
    }
};

```

---

[View on LeetCode](https://leetcode.com/problems/contains-duplicate/)