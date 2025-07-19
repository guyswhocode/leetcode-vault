---
url: https://leetcode.com/problems/invert-binary-tree
---

Difficulty: #easy
Companies: #amazon #apple #bloomberg #facebook #google #microsoft #salesforce #vmware
Lists: #blind75 #grind169 #grind75 #neetcode150

## Solution

```javascript
/**
 * 226. Invert Binary Tree
 * https://leetcode.com/problems/invert-binary-tree/
 * Difficulty: Easy
 *
 * Invert a binary tree.
 */

/**
 * Definition for a binary tree node.
 * function TreeNode(val) {
 *     this.val = val;
 *     this.left = this.right = null;
 * }
 */
/**
 * @param {TreeNode} node
 * @return {TreeNode}
 */
var invertTree = function(node) {
  if (node) [node.left, node.right] = [invertTree(node.right), invertTree(node.left)];
  return node;
};

```
