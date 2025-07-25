---
url: https://leetcode.com/problems/meeting-rooms-ii
---

Difficulty: #medium
Companies: #amazon #apple #atlassian #bloomberg #bookingcom #cisco #citadel #citrix #drawbridge #ebay #expedia #facebook #godaddy #goldman-sachs #google #lyft #microsoft #nutanix #oracle #paypal #postmates #quora #snapchat #uber #visa #yelp
Lists: #blind75 #grind169 #neetcode150

## Solution

```javascript
/**
 * 253. Meeting Rooms II
 * https://leetcode.com/problems/meeting-rooms-ii/
 * Difficulty: Medium
 *
 * Given an array of meeting time intervals intervals where intervals[i] = [starti, endi],
 * return the minimum number of conference rooms required.
 */

/**
 * @param {number[][]} intervals
 * @return {number}
 */
var minMeetingRooms = function(intervals) {
  const starts = intervals.map(([start]) => start).sort((a, b) => a - b);
  const ends = intervals.map(([, end]) => end).sort((a, b) => a - b);
  let rooms = 0;
  let startIndex = 0;
  let endIndex = 0;
  let result = 0;

  while (startIndex < intervals.length) {
    if (starts[startIndex] < ends[endIndex]) {
      rooms++;
      result = Math.max(result, rooms);
      startIndex++;
    } else {
      rooms--;
      endIndex++;
    }
  }

  return result;
};

```
