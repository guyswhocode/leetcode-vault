---
url: https://leetcode.com/problems/move-zeroes
---

Difficulty: #easy
Companies: #adobe #amazon #apple #bloomberg #cohesity #dell #ebay #facebook #goldman-sachs #google #lyft #microsoft #nutanix #oracle #paypal #qualcomm #sap #tesla #uber #yahoo #yandex #zillow
Lists: #grind169

## Solution

```javascript
/**
 * 283. Move Zeroes
 * https://leetcode.com/problems/move-zeroes/
 * Difficulty: Easy
 *
 * Given an integer array nums, move all 0's to the end of it while maintaining the
 * relative order of the non-zero elements.
 *
 * Note that you must do this in-place without making a copy of the array.
 */

/**
 * @param {number[]} nums
 * @return {void} Do not return anything, modify nums in-place instead.
 */
var moveZeroes = function(nums) {
  for (let i = 0, j = 0; i < nums.length; i++) {
    if (nums[i] !== 0) {
      [nums[i], nums[j++]] = [nums[j], nums[i]];
    }
  }
};

```
