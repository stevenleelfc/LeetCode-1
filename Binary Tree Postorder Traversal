/*Given a binary tree, return the postorder traversal of its nodes' values.*/

/* This is the first intenative version using just one stack. In this method, there are two pointers, pre and current;
when up  to bottom, the pre is the parent of current; when bottom to up, pre is the child of current.*/

/**
 * Definition for binary tree
 * public class TreeNode {
 *     int val;
 *     TreeNode left;
 *     TreeNode right;
 *     TreeNode(int x) { val = x; }
 * }
 */
public class Solution {
    public ArrayList<Integer> postorderTraversal(TreeNode root) {
        ArrayList<Integer> result = new ArrayList<Integer>();
        if(null==root)
            return result;
        Stack<TreeNode> nodes= new Stack<TreeNode>();
        TreeNode current=root;
        TreeNode pre=null;
        nodes.push(current);
        while(false==nodes.empty()){
            current=nodes.peek();
            if(null==pre || current==pre.left || current==pre.right){
                if(null!=current.left)
                    nodes.push(current.left);
                else if(null!=current.right)
                    nodes.push(current.right);
            }
            else if(pre==current.left){
                if(null!=current.right)
                    nodes.push(current.right);
            }
            else{
                result.add(current.val);
                nodes.pop();
            }
            pre=current;
        }
        return result;
    }
}
