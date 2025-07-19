---
url: https://leetcode.com/problems/valid-anagram
---

Difficulty: #easy
Companies: #amazon #apple #bloomberg #cisco #docusign #expedia #facebook #goldman-sachs #google #microsoft #morgan-stanley #oracle #paypal #servicenow #snapchat #uber #yahoo #yelp #zulily
Lists: #blind75 #grind169 #grind75 #neetcode150

## Solution

```javascript
/**
 * 242. Valid Anagram
 * https://leetcode.com/problems/valid-anagram/
 * Difficulty: Easy
 *
 * Given two strings s and t, return true if t is an anagram of s, and false otherwise.
 */

/**
 * @param {string} s
 * @param {string} t
 * @return {boolean}
 */
var isAnagram = function(s, t) {
  const sort = str => str.split('').sort().join('');
  return sort(s) === sort(t);
};

```
