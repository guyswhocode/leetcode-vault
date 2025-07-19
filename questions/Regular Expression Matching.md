---
url: https://leetcode.com/problems/regular-expression-matching
---

Difficulty: #hard
Companies: #adobe #airbnb #alibaba #amazon #apple #bloomberg #bytedance #coursera #databricks #ebay #facebook #flipkart #google #houzz #lyft #microsoft #oracle #palantir-technologies #pocket-gems #twitter #uber #zulily
Lists: #neetcode150

## Solution

```javascript
/**
 * 10. Regular Expression Matching
 * https://leetcode.com/problems/regular-expression-matching/
 * Difficulty: Hard
 *
 * Given an input string s and a pattern p, implement regular expression
 * matching with support for '.' and '*' where:
 *
 * '.' Matches any single character.
 * '*' Matches zero or more of the preceding element.
 *
 * The matching should cover the entire input string (not partial).
 */

/**
 * @param {string} s
 * @param {string} p
 * @return {boolean}
 */
var isMatch = function(s, p) {
  return new RegExp(`^${p}$`).test(s);
};

```
