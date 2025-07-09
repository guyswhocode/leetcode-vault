---
url: https://leetcode.com/problems/inorder-successor-in-bst
---

Difficulty: #medium
Companies: #amazon #bloomberg #citadel #facebook #google #microsoft #palantir-technologies #pocket-gems #quip #zillow
Lists: #grind169

## Solution

```javascript
/**
 * 285. Inorder Successor in BST
 * https://leetcode.com/problems/inorder-successor-in-bst/
 * Difficulty: Medium
 *
 * Given the root of a binary search tree and a node p in it, return the in-order successor of
 * that node in the BST. If the given node has no in-order successor in the tree, return null.
 *
 * The successor of a node p is the node with the smallest key greater than p.val.
 */

/**
 * Definition for a binary tree node.
 * function TreeNode(val) {
 *     this.val = val;
 *     this.left = this.right = null;
 * }
 */
/**
 * @param {TreeNode} root
 * @param {TreeNode} p
 * @return {TreeNode}
 */
var inorderSuccessor = function(root, p) {
  let successor = null;
  while (root) {
    if (p.val < root.val) {
      successor = root;
      root = root.left;
    } else {
      root = root.right;
    }
  }
  return successor;
};

```
