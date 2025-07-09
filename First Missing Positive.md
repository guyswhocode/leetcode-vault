---
url: https://leetcode.com/problems/first-missing-positive
---

Difficulty: #hard
Companies: #adobe #amazon #apple #bloomberg #bytedance #databricks #ebay #facebook #google #grab #microsoft #morgan-stanley #oracle #pocket-gems #salesforce #sap #tesla #twitch #uber #vmware #wayfair #wish
Lists: #grind169

## Solution

```javascript
/**
 * 41. First Missing Positive
 * https://leetcode.com/problems/first-missing-positive/
 * Difficulty: Hard
 *
 * Given an unsorted integer array nums, return the smallest missing positive integer.
 *
 * You must implement an algorithm that runs in O(n) time and uses constant extra space.
 */

/**
 * @param {number[]} nums
 * @return {number}
 */
var firstMissingPositive = function(nums) {
  let i = 0;

  while (i < nums.length) {
    if (nums[i] > 0 && nums[i] <= nums.length && nums[nums[i] - 1] !== nums[i]) {
      [nums[nums[i] - 1], nums[i]] = [nums[i], nums[nums[i] - 1]];
    } else {
      i++;
    }
  }

  for (i = 0; i < nums.length; i++) {
    if (nums[i] !== i + 1) {
      return i + 1;
    }
  }

  return i + 1;
};

```
