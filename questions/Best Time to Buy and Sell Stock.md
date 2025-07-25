---
url: https://leetcode.com/problems/best-time-to-buy-and-sell-stock
---

Difficulty: #easy
Companies: #adobe #akuna-capital #alibaba #amazon #apple #atlassian #audible #blackrock #bloomberg #bytedance #cisco #citadel #deutsche-bank #doordash #expedia #facebook #goldman-sachs #google #grab #groupon #intel #jpmorgan #linkedin #lyft #microsoft #morgan-stanley #oracle #paypal #redfin #sap #snapchat #tableau #tencent #uber #visa #vmware #yahoo #zillow
Lists: #blind75 #grind169 #grind75 #neetcode150

## Solution

```javascript
/**
 * 121. Best Time to Buy and Sell Stock
 * https://leetcode.com/problems/best-time-to-buy-and-sell-stock/
 * Difficulty: Easy
 *
 * You are given an array prices where prices[i] is the price of a given stock
 * on the ith day.
 *
 * You want to maximize your profit by choosing a single day to buy one stock
 * and choosing a different day in the future to sell that stock.
 *
 * Return the maximum profit you can achieve from this transaction. If you
 * cannot achieve any profit, return 0.
 */

/**
 * @param {number[]} prices
 * @return {number}
 */
var maxProfit = function(prices) {
  let max = 0;

  for (let i = 0, min = prices[0]; i < prices.length; i++) {
    min = Math.min(min, prices[i]);
    max = Math.max(max, prices[i] - min);
  }

  return max;
};

```
