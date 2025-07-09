---
url: https://leetcode.com/problems/kth-largest-element-in-an-array
---

Difficulty: #medium
Companies: #adobe #airbnb #alibaba #amazon #apple #atlassian #baidu #bloomberg #bytedance #ebay #expedia #facebook #goldman-sachs #google #grab #jpmorgan #linkedin #microsoft #oracle #pocket-gems #salesforce #snapchat #spotify #tencent #uber #vmware #yahoo
Lists: #grind169 #neetcode150

## Solution

```javascript
/**
 * 215. Kth Largest Element in an Array
 * https://leetcode.com/problems/kth-largest-element-in-an-array/
 * Difficulty: Medium
 *
 * Given an integer array nums and an integer k, return the kth largest element in the array.
 *
 * Note that it is the kth largest element in the sorted order, not the kth distinct element.
 */

/**
 * @param {number[]} nums
 * @param {number} k
 * @return {number}
 */
var findKthLargest = function(nums, k) {
  return nums.sort((a, b) => a - b)[nums.length - k];
};

```
