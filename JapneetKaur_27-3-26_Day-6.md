# Day 6 - POTD

## Problem
Check if N and Its Double Exist

## Code
```cpp
class Solution { 
public:  
    bool checkIfExist(vector<int>& arr) {
        unordered_map<int, int>mpp;
        for(int i = 0; i < arr.size(); i++){
            mpp[arr[i]]++;
        }

        for(int i = 0; i < arr.size(); i++){
            int x = arr[i];
            
            if(mpp.find(2*x) != mpp.end()){
                if(2*x!=x || mpp[x] > 1) return true;
            }

            if(x%2==0){
                if(mpp.find(x/2) != mpp.end()){
                    if(x/2 != x || mpp[x] > 1) return true;
                }
            }
            
        }

        return false;
    }
};
```

## Screenshot
<img width="1918" height="868" alt="Screenshot 2026-03-27 233221" src="https://github.com/user-attachments/assets/46048d06-5eea-436b-bc23-b7c9a1c1a4e5" />
