---
url: https://leetcode.com/problems/median-of-two-sorted-arrays
---

Difficulty: #hard
Companies: #adobe #airbnb #alibaba #amazon #apple #bloomberg #bytedance #didi #dropbox #ebay #facebook #garena #godaddy #goldman-sachs #google #houzz #huawei #jpmorgan #microsoft #oracle #rubrik #tencent #two-sigma #uber #visa #vmware #yahoo #yandex #zenefits #zillow #zulily
Lists: #grind169 #neetcode150

## Solution

```javascript
/**
 * 4. Median of Two Sorted Arrays
 * https://leetcode.com/problems/median-of-two-sorted-arrays/
 * Difficulty: Hard
 *
 * There are two sorted arrays nums1 and nums2 of size m and n respectively.
 *
 * Find the median of the two sorted arrays.
 * The overall run time complexity should be O(log (m+n)).
 *
 * You may assume nums1 and nums2 cannot be both empty.
 */

/**
 * @param {number[]} nums1
 * @param {number[]} nums2
 * @return {number}
 */
var findMedianSortedArrays = function(nums1, nums2) {
  const sorted = [...nums1, ...nums2].sort((a, b) => a - b);
  const index = Math.floor((sorted.length - 1) / 2);

  return sorted.length % 2 === 0
    ? (sorted[index] + sorted[index + 1]) / 2
    : sorted[index];
};

```
