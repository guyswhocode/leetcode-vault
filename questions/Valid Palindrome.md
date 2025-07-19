---
url: https://leetcode.com/problems/valid-palindrome
---

Difficulty: #easy
Companies: #adobe #amazon #apple #bloomberg #cisco #ebay #facebook #google #linkedin #microsoft #oracle #uber #wayfair #wish #yandex #zenefits
Lists: #blind75 #grind169 #grind75 #neetcode150

## Solution

```javascript
/**
 * 125. Valid Palindrome
 * https://leetcode.com/problems/valid-palindrome/
 * Difficulty: Easy
 *
 * A phrase is a palindrome if, after converting all uppercase letters into lowercase letters and
 * removing all non-alphanumeric characters, it reads the same forward and backward. Alphanumeric
 * characters include letters and numbers.
 *
 * Given a string s, return true if it is a palindrome, or false otherwise.
 */

/**
 * @param {string} s
 * @return {boolean}
 */
var isPalindrome = function(s) {
  const string = s.replace(/[^A-Z\d]+/ig, '').toLowerCase();
  return string.split('').reverse().join('') === string;
};

```
