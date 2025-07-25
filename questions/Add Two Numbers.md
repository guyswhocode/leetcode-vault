---
url: https://leetcode.com/problems/add-two-numbers
---

Difficulty: #medium
Companies: #adobe #aetion #airbnb #alibaba #amazon #apple #baidu #bloomberg #bytedance #capital-one #cisco #dell #docusign #ebay #facebook #flipkart #google #grab #huawei #ibm #intel #lyft #mathworks #microsoft #nvidia #oracle #paypal #qualcomm #redfin #salesforce #servicenow #uber #vmware #wish #yahoo #yandex #zoho
Lists: #grind169 #neetcode150

## Solution

```javascript
/**
 * 2. Add Two Numbers
 * https://leetcode.com/problems/add-two-numbers/
 * Difficulty: Medium
 *
 * You are given two non-empty linked lists representing two non-negative integers.
 *
 * The digits are stored in reverse order, and each of their nodes contains a single digit.
 * Add the two numbers and return the sum as a linked list.
 *
 * You may assume the two numbers do not contain any leading zero, except the number 0 itself.
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
var addTwoNumbers = function(l1, l2) {
  const result = new ListNode();

  for (let tail = result, carry = 0; l1 || l2 || carry;) {
    const value = (l1?.val ?? 0) + (l2?.val ?? 0) + carry;
    tail.next = new ListNode(value % 10);
    tail = tail.next;
    carry = value >= 10 ? 1 : 0;
    [l1, l2] = [l1 && l1.next, l2 && l2.next];
  }

  return result.next;
};

```
