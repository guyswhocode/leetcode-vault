---
url: https://leetcode.com/problems/squares-of-a-sorted-array
---

Difficulty: #easy
Companies: #adobe #amazon #apple #bloomberg #bytedance #ebay #electronic-arts #facebook #google #microsoft #nutanix #oracle #paypal #splunk #twitch #uber #vmware
Lists: #grind169

## Solution

```javascript
/**
 * 977. Squares of a Sorted Array
 * https://leetcode.com/problems/squares-of-a-sorted-array/
 * Difficulty: Easy
 *
 * Given an array of integers A sorted in non-decreasing order,
 * return an array of the squares of each number,
 * also in sorted non-decreasing order.
 */

/**
 * @param {number[]} A
 * @return {number[]}
 */
var sortedSquares = function(A) {
  return A.map(n => Math.pow(n, 2)).sort((a, b) => a - b);
};

```
