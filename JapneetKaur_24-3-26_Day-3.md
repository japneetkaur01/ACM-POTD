# Day 3 - POTD

## Problem
Best Time to Buy and Sell Stock

## Code
```cp
class Solution {
public:
    int maxProfit(vector<int>& prices) {
        int minn = INT_MAX;
        int profit;
        for(int i = 0; i < prices.size(); i++){
            minn = min(minn, prices[i]);
            profit = max(profit, prices[i] - minn);
        }

        return profit;
    }
};
```

## Screenshot
<img width="1885" height="812" alt="Screenshot 2026-03-25 000836" src="https://github.com/user-attachments/assets/855c5c42-9aca-4f3e-9eb6-9addf656ae46" />
