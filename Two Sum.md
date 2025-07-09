---
url: https://leetcode.com/problems/two-sum
---

Difficulty: #easy
Companies: #adobe #aetion #affirm #airbnb #alibaba #amazon #apple #audible #baidu #blackrock #bloomberg #bookingcom #box #bytedance #cisco #citadel #cloudera #deutsche-bank #didi #drawbridge #dropbox #ebay #emc #expedia #facebook #factset #ge-digital #godaddy #goldman-sachs #google #groupon #huawei #ibm #indeed #intel #intuit #jpmorgan #linkedin #lyft #mathworks #microsoft #morgan-stanley #netease #nvidia #oracle #paypal #qualcomm #quora #radius #roblox #salesforce #samsung #sap #servicenow #snapchat #splunk #spotify #tableau #tencent #twilio #twitter #uber #valve #visa #vmware #wish #works-applications #yahoo #yandex #yelp #zillow #zoho
Lists: #blind75 #grind169 #grind75 #neetcode150

## Solution

```javascript
/**
 * 1. Two Sum
 * https://leetcode.com/problems/two-sum/
 * Difficulty: Easy
 *
 * Given an array of integers `nums` and an integer `target`, return indices
 * of the two numbers such that they add up to `target`.
 *
 * You may assume that each input would have exactly one solution, and you
 * may not use the same element twice.
 *
 * You can return the answer in any order.
 */

/**
 * @param {number[]} nums
 * @param {number} target
 * @return {number[]}
 */
var twoSum = function(nums, target) {
  const map = new Map();

  for (let i = 0; i < nums.length; i++) {
    const diff = target - nums[i];

    if (map.has(diff)) {
      return [map.get(diff), i];
    }

    map.set(nums[i], i);
  }
};

```
