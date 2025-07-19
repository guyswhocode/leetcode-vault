---
url: https://leetcode.com/problems/reverse-words-in-a-string
---

Difficulty: #medium
Companies: #amazon #apple #bloomberg #cisco #citadel #facebook #google #huawei #microsoft #nvidia #oracle #qualcomm #salesforce #snapchat #vmware #yelp #zillow

## Solution

```javascript
/**
 * 151. Reverse Words in a String
 * https://leetcode.com/problems/reverse-words-in-a-string/
 * Difficulty: Medium
 *
 * Given an input string, reverse the string word by word.
 */

/**
 * @param {string} s
 * @return {string}
 */
var reverseWords = function(s) {
  return s.trim().replace(/\s+/g, ' ').split(/\s/).reverse().join(' ');
};

```
