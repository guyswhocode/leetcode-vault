---
url: https://leetcode.com/problems/maximum-subarray
---

Difficulty: #easy
Companies: #adobe #alibaba #amazon #apple #asana #atlassian #bloomberg #bytedance #capital-one #cisco #citadel #ebay #expedia #facebook #goldman-sachs #google #ibm #intel #jpmorgan #linkedin #microsoft #morgan-stanley #nvidia #oracle #palantir-technologies #paypal #qualcomm #salesforce #sap #two-sigma #uber #visa #wayfair #yahoo #zillow
Lists: #blind75 #grind169 #grind75 #neetcode150

## Solution

```javascript
/**
 * 53. Maximum Subarray
 * https://leetcode.com/problems/maximum-subarray/
 * Difficulty: Easy
 *
 * Given an integer array `nums`, find the contiguous subarray (containing at
 * least one number) which has the largest sum and return its sum.
 *
 * A subarray is a contiguous part of an array.
 */

/**
 * @param {number[]} nums
 * @return {number}
 */
var maxSubArray = function(nums) {
  for (let i = 1; i < nums.length; i++) {
    if (nums[i - 1] > 0) {
      nums[i] += nums[i - 1];
    }
  }

  return Math.max(...nums);
};

```
