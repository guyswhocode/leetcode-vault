---
url: https://leetcode.com/problems/reverse-linked-list
---

Difficulty: #easy
Companies: #adobe #alibaba #amazon #apple #bloomberg #bytedance #cisco #citrix #docusign #ebay #electronic-arts #facebook #factset #goldman-sachs #google #intel #mathworks #microsoft #nvidia #oracle #paypal #qualcomm #snapchat #spotify #tencent #tripadvisor #twitter #uber #visa #vmware #yahoo #yandex #yelp #zenefits
Lists: #blind75 #grind169 #grind75 #neetcode150

## Solution

```javascript
/**
 * 206. Reverse Linked List
 * https://leetcode.com/problems/reverse-linked-list/
 * Difficulty: Easy
 *
 * Given the head of a singly linked list, reverse the list, and return the reversed list.
 */

/**
 * Definition for singly-linked list.
 * function ListNode(val, next) {
 *     this.val = (val===undefined ? 0 : val)
 *     this.next = (next===undefined ? null : next)
 * }
 */
/**
 * @param {ListNode} head
 * @return {ListNode}
 */
var reverseList = function(head) {
  let prev = null;
  let tail = head;

  while (tail) {
    const next = tail.next;
    tail.next = prev;
    prev = tail;
    tail = next;
  }

  return prev;
};

```
