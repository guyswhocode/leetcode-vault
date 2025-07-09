---
url: https://leetcode.com/problems/set-matrix-zeroes
---

Difficulty: #medium
Companies: #adobe #amazon #apple #audible #docusign #expedia #facebook #microsoft #oracle #paypal #salesforce #tripadvisor
Lists: #blind75 #grind169 #neetcode150

## Solution

```javascript
/**
 * 73. Set Matrix Zeroes
 * https://leetcode.com/problems/set-matrix-zeroes/
 * Difficulty: Medium
 *
 * Given an `m x n` integer `matrix` matrix, if an element is `0`, set its entire
 * row and column to `0`'s, and return the matrix.
 *
 * You must do it in place.
 */

/**
 * @param {number[][]} matrix
 * @return {void} Do not return anything, modify matrix in-place instead.
 */
var setZeroes = function(matrix) {
  const columns = new Set();
  const rows = new Set();

  matrix.forEach((row, i) => {
    row.forEach((value, j) => {
      if (value === 0) {
        columns.add(i);
        rows.add(j);
      }
    });
  });

  [...columns].forEach(i => matrix[i].forEach((_, j) => matrix[i][j] = 0));
  matrix.forEach((_, i) => [...rows].forEach(j => matrix[i][j] = 0));

  return matrix;
};

```
