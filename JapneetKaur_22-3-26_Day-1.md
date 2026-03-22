# Day 1 - POTD

## Problem 
Remove Duplicates from Sorted Array

## Approach
Two Pointers

## Code
```cpp
class Solution {
public:
    int removeDuplicates(vector<int>& arr) {
        int i = 0;
        for(int j = i+1; j < arr.size(); j++){
            if(arr[j] != arr[i]){
                arr[i+1] = arr[j];
                i++;
            }
        }

        return (i+1);
    }    
};
```

## Screenshot
<img width="856" height="879" alt="Screenshot 2026-03-22 200912" src="https://github.com/user-attachments/assets/fb6ecf51-f4d0-42b2-a9e0-aef4f079b950" />

