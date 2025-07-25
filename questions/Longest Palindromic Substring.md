---
url: https://leetcode.com/problems/longest-palindromic-substring
---

Difficulty: #medium
Companies: #adobe #airbnb #alibaba #amazon #appdynamics #apple #bloomberg #cisco #ebay #facebook #godaddy #google #huawei #jpmorgan #mathworks #microsoft #nutanix #oracle #paypal #pure-storage #roblox #samsung #sap #servicenow #tencent #uber #vmware #wayfair #yahoo #yandex
Lists: #blind75 #grind169 #grind75 #neetcode150

## Solution

```javascript
/**
 * 5. Longest Palindromic Substring
 * https://leetcode.com/problems/longest-palindromic-substring/
 * Difficulty: Medium
 *
 * Given a string `s`, return the longest palindromic substring in `s`.
 */

/**
 * @param {string} s
 * @return {string}
 */
var longestPalindrome = function(s) {
  let result = '';

  for (let i = 0; i < s.length; i++) {
    const palindrome1 = getExtendedPalindrome(s, i, i);
    const palindrome2 = getExtendedPalindrome(s, i, i + 1);
    const longerPalindrome = palindrome1.length > palindrome2.length
      ? palindrome1
      : palindrome2;

    if (longerPalindrome.length > result.length) {
      result = longerPalindrome;
    }
  }

  return result;
};

function getExtendedPalindrome(s, start, end) {
  while (start >= 0 && end < s.length && s[start] === s[end]) {
    start--;
    end++;
  }

  return s.slice(start + 1, end);
}

```
