# Middle-of-the-Linked-List
c++

/**
 * Definition for singly-linked list.
 * struct ListNode {
 *     int val;
 *     ListNode *next;
 *     ListNode(int x) : val(x), next(NULL) {}
 * };
 */
class Solution {
public:
    ListNode* middleNode(ListNode* head) {
        ListNode *a_pointer=head;
        ListNode *b_pointer=head;
        while(b_pointer!=NULL && b_pointer->next!=NULL)
        {
            a_pointer=a_pointer->next;
            b_pointer=b_pointer->next->next;
        }
        return a_pointer;
    }
};
