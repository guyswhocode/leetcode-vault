---
url: https://leetcode.com/problems/reverse-integer
---

Difficulty: #easy
Companies: #adobe #amazon #apple #barclays #bloomberg #cisco #facebook #google #jpmorgan #lyft #microsoft #netease #oracle #uber #yahoo
Lists: #grind169 #neetcode150

## Solution

```javascript
/**
 * 7. Reverse Integer
 * https://leetcode.com/problems/reverse-integer/
 * Difficulty: Easy
 *
 * Given a signed 32-bit integer x, return x with its digits reversed.
 * If reversing x causes the value to go outside the signed 32-bit integer
 * range [-2^31, 2^31 - 1], then return 0.
 */

/**
 * @param {number} x
 * @return {number}
 */
var reverse = function(x) {
  const reversed = String(Math.abs(x)).split('').reverse().join('');

  if (reversed > Math.pow(2, 31)) {
    return 0;
  }

  return reversed * Math.sign(x);
};

```
