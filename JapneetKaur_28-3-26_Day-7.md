# Day 7 - POTD

## Problem
Increasing Triplet Subsequence

## Code
```cpp
class Solution {
public:
    bool increasingTriplet(vector<int>& nums) {
        int first = INT_MAX;
        int second = INT_MAX;
        for(int i = 0; i < nums.size(); i++){
            if(nums[i] <= first){
                first = nums[i];
            }

            else if(nums[i] <= second){
                second = nums[i];
            }

            else{
                return true;
            }
        }
        return false;
    }
};
```

## Screenshot
<img width="1919" height="876" alt="Screenshot 2026-03-28 151217" src="https://github.com/user-attachments/assets/9d986b81-9539-48bf-ab97-4117cc0395db" />
