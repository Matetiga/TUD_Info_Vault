
## Solution
- [[Ternary Operator]] = ?:
```cpp
    class Solution {
public:
    ListNode* addTwoNumbers(ListNode* l1, ListNode* l2) {
        ListNode* head = new ListNode(0);
        ListNode* curr = head;
        int carry = 0;

        while (l1 != nullptr || l2 != nullptr || carry) {

			// Ternary Operator
            int x = l1 ? l1->val : 0;
            int y = l2 ? l2->val : 0;

            int sum = x + y + carry;

            // either 1 or 0
            carry = sum / 10;

            curr->next = new ListNode(sum % 10);
            curr = curr->next;

            if (l1) l1 = l1->next;
            if (l2) l2 = l2->next;
        }

        ListNode* result = head->next;
        // test node is deleted
        delete head;
        return result;
    }
};
```