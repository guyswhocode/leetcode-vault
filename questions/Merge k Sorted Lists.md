---
url: https://leetcode.com/problems/merge-k-sorted-lists
---

Difficulty: #hard
Companies: #adobe #airbnb #alibaba #amazon #apple #atlassian #audible #bloomberg #box #bytedance #cisco #cohesity #cruise-automation #ebay #facebook #goldman-sachs #google #indeed #ixl #linkedin #lyft #mathworks #microsoft #nvidia #oracle #salesforce #sap #tableau #twitter #uber #vmware #wish #yahoo #yandex #zillow
Lists: #blind75 #grind169 #grind75 #neetcode150

## Solution

```javascript
/**
 * 23. Merge k Sorted Lists
 * https://leetcode.com/problems/merge-k-sorted-lists/
 * Difficulty: Hard
 *
 * You are given an array of k linked-lists lists, each linked-list is sorted
 * in ascending order.
 *
 * Merge all the linked-lists into one sorted linked-list and return it.
 */

/**
 * Definition for singly-linked list.
 * function ListNode(val, next) {
 *     this.val = (val===undefined ? 0 : val)
 *     this.next = (next===undefined ? null : next)
 * }
 */
/**
 * @param {ListNode[]} lists
 * @return {ListNode}
 */
var mergeKLists = function(lists) {
  const map = new Map();
  for (let list of lists) {
    while (list) {
      map.set(list.val, (map.get(list.val) || 0) + 1);
      list = list.next;
    }
  }
  const sorted = [...map].sort(([a], [b]) => a - b);
  const result = new ListNode();
  let tail = result;

  for (let [key, value] of sorted) {
    while (value--) {
      tail.next = new ListNode(key);
      tail = tail.next;
    }
  }

  return result.next;
};

```
