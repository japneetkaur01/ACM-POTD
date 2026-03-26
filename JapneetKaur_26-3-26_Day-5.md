# Day 5 - POTD

## Problem
Product of Array Except Self

## Code
```cpp
class Solution {
public:
    vector<int> productExceptSelf(vector<int>& nums) {
        vector<int> ans(nums.size(),1);

        int left = 1;
        for(int i = 0; i < nums.size(); i++){
            ans[i] = left;
            left *= nums[i];
        }

        int right = 1;
        for(int i = nums.size()-1; i >= 0; i--){
            ans[i] *= right;
            right *= nums[i];
        }

        return ans;
        
    }
};
```

## Screenshot
<img width="1918" height="871" alt="Screenshot 2026-03-26 132519" src="https://github.com/user-attachments/assets/84537689-e946-4c59-a0cb-16c2de1c8898" />

