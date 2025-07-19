---
url: https://leetcode.com/problems/trapping-rain-water
---

Difficulty: #hard
Companies: #adobe #affirm #airbnb #amazon #apple #audible #bloomberg #bytedance #citadel #databricks #dataminr #ebay #electronic-arts #facebook #flipkart #goldman-sachs #google #grab #huawei #lyft #microsoft #nvidia #oracle #palantir-technologies #qualtrics #salesforce #servicenow #snapchat #tableau #twitter #uber #visa #wish #yahoo #yandex #zenefits
Lists: #grind169 #grind75 #neetcode150

## Solution

```javascript
/**
 * 42. Trapping Rain Water
 * https://leetcode.com/problems/trapping-rain-water/
 * Difficulty: Hard
 *
 * Given n non-negative integers representing an elevation map where the
 * width of each bar is 1, compute how much water it can trap after raining.
 */

/**
 * @param {number[]} height
 * @return {number}
 */
var trap = function(height) {
  let result = 0;

  for (let left = 0, right = height.length - 1, maxL = 0, maxR = 0; left < right;) {
    maxL = Math.max(maxL, height[left]);
    maxR = Math.max(maxR, height[right]);
    result += maxL < maxR ? maxL - height[left++] : maxR - height[right--];
  }

  return result;
};

```
