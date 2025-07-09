---
url: https://leetcode.com/problems/valid-parentheses
---

Difficulty: #easy
Companies: #adobe #airbnb #akuna-capital #amazon #apple #atlassian #audible #barclays #blizzard #bloomberg #cisco #citadel #doordash #ebay #epic-systems #expedia #facebook #godaddy #goldman-sachs #google #ibm #intel #intuit #jpmorgan #linkedin #liveramp #lyft #mathworks #microsoft #morgan-stanley #oracle #paypal #postmates #riot-games #salesforce #samsung #sap #servicenow #splunk #spotify #tencent #tesla #triplebyte #twilio #twitter #uber #visa #vmware #yahoo #yandex #zenefits #zillow
Lists: #blind75 #grind169 #grind75 #neetcode150

## Solution

```javascript
/**
 * 20. Valid Parentheses
 * https://leetcode.com/problems/valid-parentheses/
 * Difficulty: Easy
 *
 * Given a string s containing just the characters '(', ')', '{', '}',
 * '[' and ']', determine if the input string is valid.
 *
 * An input string is valid if:
 * - Open brackets must be closed by the same type of brackets.
 * - Open brackets must be closed in the correct order.
 */

/**
 * @param {string} s
 * @return {boolean}
 */
var isValid = function(s) {
  const map = {
    '(': ')',
    '[': ']',
    '{': '}',
  };
  const stack = [];

  for (let i = 0; i < s.length; i++) {
    if (map[s[i]]) {
      stack.push(map[s[i]]);
    } else {
      if (stack.pop() !== s[i]) {
        return false;
      }
    }
  }

  return stack.length === 0;
};

```
