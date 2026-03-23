# Day 2 - POTD

## Problem
Subarray Sum Equals K

## Approach 
Prefix + Hashmap

## Code
```cpp
class Solution {
public:
    int subarraySum(vector<int>& nums, int k) {
        int count = 0;
        int sum = 0;
        unordered_map<int, int> freq;
        freq[0] = 1;
        for(int i = 0; i < nums.size(); i++){
            sum+=nums[i];
            if(freq.find(sum-k)!=freq.end()){
                count+=freq[sum-k];
            }
            freq[sum]++;
        }


        return count;
    }
};
```

## Screenshot
<img width="1913" height="869" alt="Screenshot 2026-03-23 231236" src="https://github.com/user-attachments/assets/378c9f41-4bc3-457b-b38e-9c10db529fb2" />
