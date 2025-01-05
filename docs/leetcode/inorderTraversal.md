### 题目描述
给定一个二叉树的根节点 `root` ，返回 *它的 **中序** 遍历* 。
### 思路
直接从根节点开始递归即可
### 题解
```java
class Solution {
    public List<Integer> inorderTraversal(TreeNode root) {
        List<Integer> list = new ArrayList<>();
        inorder(root, list);
        return list;
    }

    public void inorder(TreeNode node, List<Integer> list) {
        if (node == null) return;
        inorder(node.left, list);
        list.add(node.val);
        inorder(node.right, list);        
    }
}
```
