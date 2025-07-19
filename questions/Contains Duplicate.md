---
url: https://leetcode.com/problems/contains-duplicate
---

Difficulty: #easy
Companies: #adobe #airbnb #amazon #apple #bloomberg #facebook #microsoft #oracle #palantir-technologies #yahoo
Lists: #blind75 #grind169 #grind75 #neetcode150

## Solution

```javascript
/**
 * 217. Contains Duplicate
 * https://leetcode.com/problems/contains-duplicate/
 * Difficulty: Easy
 *
 * Given an integer array `nums`, return `true` if any value appears at least
 * twice in the array, and return `false` if every element is distinct.
 */

/**
 * @param {number[]} nums
 * @return {boolean}
 */
var containsDuplicate = function(nums) {
  return new Set(nums).size !== nums.length;
};

```
