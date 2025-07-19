---
url: https://leetcode.com/problems/group-anagrams
---

Difficulty: #medium
Companies: #adobe #affirm #amazon #apple #bloomberg #bookingcom #cisco #docusign #ebay #electronic-arts #facebook #goldman-sachs #google #hulu #intuit #mathworks #microsoft #nutanix #oracle #qualtrics #salesforce #servicenow #snapchat #tesla #twilio #uber #visa #vmware #wish #yahoo #yandex #yelp #zulily
Lists: #blind75 #grind169 #neetcode150

## Solution

```javascript
/**
 * 49. Group Anagrams
 * https://leetcode.com/problems/group-anagrams/
 * Difficulty: Medium
 *
 * Given an array of strings `strs`, group the anagrams together. You can return the
 * answer in any order.
 *
 * An Anagram is a word or phrase formed by rearranging the letters of a different
 * word or phrase, typically using all the original letters exactly once.
 */

/**
 * @param {string[]} strs
 * @return {string[][]}
 */
var groupAnagrams = function(strs) {
  const map = {};

  strs.forEach(str => {
    const key = [...str].sort();
    map[key] = map[key] ? [...map[key], str] : [str];
  });

  return Object.values(map);
};

```
