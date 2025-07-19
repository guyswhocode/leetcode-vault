---
url: https://leetcode.com/problems/longest-substring-without-repeating-characters
---

Difficulty: #medium
Companies: #adobe #alation #alibaba #amazon #apple #atlassian #baidu #bloomberg #bytedance #cisco #coupang #ebay #expedia #facebook #goldman-sachs #google #huawei #microsoft #oracle #paypal #salesforce #samsung #sap #snapchat #spotify #twitch #uber #vmware #yahoo #yandex #yelp #zillow #zoho
Lists: #blind75 #grind169 #grind75 #neetcode150

## Solution

```javascript
/**
 * 3. Longest Substring Without Repeating Characters
 * https://leetcode.com/problems/longest-substring-without-repeating-characters/
 * Difficulty: Medium
 *
 * Given a string `s`, find the length of the longest substring without repeating characters.
 */

/**
 * @param {string} s
 * @return {number}
 */
var lengthOfLongestSubstring = function(s) {
  const map = {};
  let offset = 0;

  return s.split('').reduce((max, value, i) => {
    offset = map[value] >= offset ? map[value] + 1 : offset;
    map[value] = i;
    return Math.max(max, i - offset + 1);
  }, 0);
};

```
