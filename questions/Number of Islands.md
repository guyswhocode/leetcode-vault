---
url: https://leetcode.com/problems/number-of-islands
---

Difficulty: #medium
Companies: #adobe #affirm #alibaba #amazon #appdynamics #apple #arista-networks #atlassian #audible #blackrock #bloomberg #bytedance #cisco #citadel #citrix #cohesity #cruise-automation #doordash #ebay #electronic-arts #evernote #expedia #facebook #godaddy #goldman-sachs #google #houzz #hulu #jpmorgan #linkedin #liveramp #lyft #mathworks #microsoft #nutanix #nvidia #oracle #palantir-technologies #paypal #qualtrics #roblox #salesforce #servicenow #snapchat #splunk #spotify #square #sumologic #tableau #twitch #twitter #uber #visa #vmware #wish #yahoo #zenefits #zulily
Lists: #blind75 #grind169 #grind75 #neetcode150

## Solution

```javascript
/**
 * 200. Number of Islands
 * https://leetcode.com/problems/number-of-islands/
 * Difficulty: Medium
 *
 * Given an m x n 2D binary grid grid which represents a map of '1's (land) and '0's (water),
 * return the number of islands.
 *
 * An island is surrounded by water and is formed by connecting adjacent lands horizontally
 * or vertically. You may assume all four edges of the grid are all surrounded by water.
 */

/**
 * @param {character[][]} grid
 * @return {number}
 */
var numIslands = function(grid) {
  let count = 0;

  for (let i = 0; i < grid.length; i++) {
    for (let j = 0; j < grid[i].length; j++) {
      if (grid[i][j] === '1') {
        count++;
        dfs(i, j);
      }
    }
  }

  function dfs(i, j) {
    if (i < 0 || i >= grid.length || j < 0 || j >= grid[i].length || grid[i][j] === '0') {
      return;
    }

    grid[i][j] = '0';

    dfs(i + 1, j);
    dfs(i - 1, j);
    dfs(i, j + 1);
    dfs(i, j - 1);
  }

  return count;
};

```
