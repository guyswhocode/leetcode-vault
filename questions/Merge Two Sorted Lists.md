---
url: https://leetcode.com/problems/merge-two-sorted-lists
---

Difficulty: #easy
Companies: #adobe #airbnb #alibaba #amazon #apple #arista-networks #atlassian #bloomberg #bytedance #capital-one #cisco #ebay #facebook #google #huawei #indeed #intel #linkedin #lyft #microsoft #oracle #paypal #samsung #tencent #uber #visa #vmware #yahoo #yandex
Lists: #blind75 #grind169 #grind75 #neetcode150

## Solution

```javascript
/**
 * 21. Merge Two Sorted Lists
 * https://leetcode.com/problems/merge-two-sorted-lists/
 * Difficulty: Easy
 *
 * Merge two sorted linked lists and return it as a sorted list.
 * The list should be made by splicing together the nodes of the
 * first two lists.
 */

/**
 * Definition for singly-linked list.
 * function ListNode(val, next) {
 *     this.val = (val===undefined ? 0 : val)
 *     this.next = (next===undefined ? null : next)
 * }
 */
/**
 * @param {ListNode} l1
 * @param {ListNode} l2
 * @return {ListNode}
 */
var mergeTwoLists = function(l1, l2) {
  if (!l1 || !l2) {
    return l1 || l2;
  }

  if (l1.val > l2.val) {
    [l2, l1] = [l1, l2];
  }

  l1.next = mergeTwoLists(l1.next, l2);

  return l1;
};

```
