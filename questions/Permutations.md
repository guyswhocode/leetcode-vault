---
url: https://leetcode.com/problems/permutations
---

Difficulty: #medium
Companies: #adobe #amazon #apple #atlassian #bloomberg #bytedance #cisco #ebay #facebook #garena #godaddy #goldman-sachs #google #linkedin #microsoft #netease #oracle #paypal #salesforce #sap #uber #vmware #yahoo
Lists: #grind169 #grind75 #neetcode150

## Solution

```javascript
/**
 * 46. Permutations
 * https://leetcode.com/problems/permutations/
 * Difficulty: Medium
 *
 * Given an array nums of distinct integers, return all the possible permutations.
 * You can return the answer in any order.
 */

/**
 * @param {number[]} nums
 * @return {number[][]}
 */
var permute = function(nums) {
  const result = [];
  backtrack(result, nums);
  return result;
};

function backtrack(result, nums, order = []) {
  if (!nums.length) {
    result.push(order);
  } else {
    for (let i = 0; i < nums.length; i++) {
      backtrack(
        result,
        [...nums.slice(0, i), ...nums.slice(i + 1)],
        [...order, nums[i]]
      );
    }
  }
}

```
