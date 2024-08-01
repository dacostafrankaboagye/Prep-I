## 1379. Find a Corresponding Node of a Binary Tree in a Clone of That Tree

Given two binary trees original and cloned and given a reference to a node target in the original tree.

The cloned tree is a copy of the original tree.

Return a reference to the same node in the cloned tree.

Note that you are not allowed to change any of the two trees or the target node and the answer must be a reference to a node in the cloned tree.




Input: tree = [8,null,6,null,5,null,4,null,3,null,2,null,1], target = 4
Output: 4
 

Constraints:

The number of nodes in the tree is in the range [1, 104].
The values of the nodes of the tree are unique.
target node is a node from the original tree and is not null.
 

Follow up: Could you solve the problem if repeated values on the tree are allowed?

```java
/**
 * Definition for a binary tree node.
 * public class TreeNode {
 *     int val;
 *     TreeNode left;
 *     TreeNode right;
 *     TreeNode(int x) { val = x; }
 * }
 */

class Solution {
    static int sVal ;

    static TreeNode dfs(TreeNode aNode){
        // b-1
        if(aNode == null){
            return null;
        }
        // b-2
        if(aNode.val == sVal){
            return aNode;
        }

        TreeNode left = dfs(aNode.left);
        if(left != null){
            return left;
        }

        return dfs(aNode.right);

        
        
    }


    public final TreeNode getTargetCopy(final TreeNode original, final TreeNode cloned, final TreeNode target) {
        sVal = target.val;
        TreeNode result = dfs(cloned);
        return result;
        
    }
}
```
