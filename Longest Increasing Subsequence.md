---
url: https://leetcode.com/problems/longest-increasing-subsequence
---

Difficulty: #medium
Companies: #adobe #amazon #apple #atlassian #ebay #facebook #google #microsoft #oracle #salesforce #uber #vmware
Lists: #blind75 #grind169 #neetcode150

## Solution

```javascript
/**
 * 300. Longest Increasing Subsequence
 * https://leetcode.com/problems/longest-increasing-subsequence/
 * Difficulty: Medium
 *
 * Given an integer array nums, return the length of the longest strictly increasing subsequence.
 */

/**
 * @param {number[]} nums
 * @return {number}
 */
var lengthOfLIS = function(nums) {
  if (!nums.length) return 0;

  const dp = new Array(nums.length).fill(1);
  for (let i = 1; i < nums.length; i++) {
    for (let j = 0; j < i; j++) {
      if (nums[i] > nums[j]) {
        dp[i] = Math.max(dp[i], dp[j] + 1);
      }
    }
  }

  return Math.max(...dp);
};

```
