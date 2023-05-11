## Problem 
Given a sorted array of distinct integers and a target value, return the index if the target is found. If not, return the index where it would be if it were inserted in order.

You must write an algorithm with `O(log n)` runtime complexity.

## Solution
Binary search is the best solution to this problem 

```
class Solution {
public:
    int searchInsert(vector<int>& nums, int target) {
        int max = INT_MAX;
        int ans;
        for(int i=0;i<nums.size();i++)
        {
            if(nums[i]==target)
            {
               ans = i;
            }
            else if(i>INT_MAX && target>i)
            {
                target = nums[i+1];
                ans = i+1;
            }
        }
        return ans;
        
        
    }
};
```
