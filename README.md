# leetcode876-midLinkedList

    # Definition for singly-linked list.
    # class ListNode:
    #     def __init__(self, val=0, next=None):
    #         self.val = val
    #         self.next = next
    class Solution:
        def middleNode(self, head: Optional[ListNode]) -> Optional[ListNode]:
            slow = fast =head
            while fast and fast.next:
                slow = slow.next
                fast = fast.next.next
            return slow
            
            1   2   3   4   5   6
           s/f
                s   f
                    s       f
                        s           (f=none)
            fast run twice as slow, when fast reach the end. The slow just get to the middle
