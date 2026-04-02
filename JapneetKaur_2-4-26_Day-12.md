# Day 12 - POTD

## Problem
Remove Duplicates from Sorted List

## Code
```cpp
class Solution {
public:
    ListNode* deleteDuplicates(ListNode* head) {
        ListNode* current = head;
        while(current!=nullptr && current->next!=nullptr){
            if(current->val == current->next->val){
                current->next = current->next->next;
            }

            else{
                current = current->next;
            }
        }

        return head;
    }
};
```
## Screenshot
<img width="1910" height="875" alt="image" src="https://github.com/user-attachments/assets/04a7b719-8217-4e51-ab06-90f384e4f476" />
