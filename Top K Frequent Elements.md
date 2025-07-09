---
url: https://leetcode.com/problems/top-k-frequent-elements
---

Difficulty: #medium
Companies: #amazon #apple #bloomberg #bytedance #ebay #facebook #goldman-sachs #google #hulu #linkedin #microsoft #oracle #pocket-gems #snapchat #spotify #uber #vmware #yahoo #yelp
Lists: #blind75 #neetcode150

## Solution

```javascript
/**
 * 347. Top K Frequent Elements
 * https://leetcode.com/problems/top-k-frequent-elements/
 * Difficulty: Medium
 *
 * Given an integer array `nums` and an integer `k`, return the `k` most
 * frequent elements. You may return the answer in any order.
 */

/**
 * @param {number[]} nums
 * @param {number} k
 * @return {number[]}
 */
var topKFrequent = function(nums, k) {
  const map = new Map();

  nums.forEach(value => map.set(value, (map.get(value) || 0) + 1));

  return [...map]
    .sort((a, b) => b[1] - a[1])
    .slice(0, k)
    .map(([value]) => value)
};

```
