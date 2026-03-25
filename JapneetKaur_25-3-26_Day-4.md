# Day 4 - POTD

## Problem
Two Sum II – Input Array Is Sorted

## Code
```cp
class Solution {
public:
    vector<int> twoSum(vector<int>& numbers, int target) {
        vector<int> ans;
        unordered_map<int, int> hsh;
        for(int i = 0; i < numbers.size(); i++){
            int complement = target - numbers[i];
            if(hsh.find(complement) != hsh.end()){
                ans.push_back(hsh[complement]+1);
                ans.push_back(i+1);
            }

            hsh[numbers[i]] = i;
        }
        return ans;
    }
};
```

## Screenshot
<img width="1887" height="801" alt="image" src="https://github.com/user-attachments/assets/55eda979-9760-4bb1-9a46-29a2d52ee5eb" />
