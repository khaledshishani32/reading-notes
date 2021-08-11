# A Binary Tree
---
## Why is it called a tree?
#### It’s called a “tree” because it vaguely resembles an inverted tree trunk with branches.
#### The word “binary” indicates that each “node” in the tree can have at most 2 children (left or right).
#### Nodes can have 0, 1 or 2 children. Nodes that do not have any children are sometimes also called “leaves”.
#### The single node at the top is called the “root” node, and it typically where operations like search, insertion .
---
## Implementation Tree Node  
#### #simple class representing a node within a binary tree.
#### class TreeNode:
####    def __init__(self, key):
####        self.key = key
####        self.left = None
####        self.right = None
#### #create objects representing each node of the above tree
#### node0 = TreeNode(3)
#### node1 = TreeNode(4)
#### node2 = TreeNode(5)
#### #connect the nodes by setting the .left and .right properties of the root node. And we're done! We can create a new variable tree which simply points to the root node, and use it to access all the nodes within the tree.
#### node0.left = node1
#### node0.right = node2
#### #Going forward, we'll use the term "tree" to refer to the root node. The term "node" can refer to any node in a tree, not necessarily the root.

---
## Traversing a Binary Tree

#### A traversal refers to the process of visiting each node of a tree exactly once. Visiting a node generally refers to adding the node’s key to a list. There are three ways to traverse a binary tree and return the list of visited keys:
## Inorder traversal
- Traverse the left subtree recursively inorder.
- Traverse the current node.
- Traverse the right subtree recursively inorder.
 


## Preorder traversal
- Traverse the current node.
- Traverse the left subtree recursively preorder.
- Traverse the right subtree recursively preorder.
 



## Postorder traversal
- Traverse the left subtree recursively postorder.
- Traverse the right subtree recursively postorder.
- Traverse the current node.


---
## #implementation of inorder traversal of a binary tre

#### def traverse_in_order(node):
####   &nbsp; &nbsp; &nbsp; if node is None: 
####   &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;    return []
####   &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;   return(traverse_in_order(node.left) + 
####   &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;         [node.key] + 
####  &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;          traverse_in_order(node.right))

---
## A Binary Search Tree (BST)
#### A binary search tree or BST is a binary tree that satisfies the following conditions:
- The left subtree of any node only contains nodes with keys less than the node’s key
- The right subtree of any node only contains nodes with keys greater than the node’s key
 


#### def is_bst(node):
####  &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;  if node is None:
####   &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;  &nbsp; &nbsp;  &nbsp; &nbsp;    return True, None, None
    
####  &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;  is_bst_l, min_l, max_l = is_bst(node.left)
####  &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;  is_bst_r, min_r, max_r = is_bst(node.right)
    
####  &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;  is_bst_node = (is_bst_l and is_bst_r and 
####  &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;  &nbsp; &nbsp;  &nbsp; &nbsp;            (max_l is None or node.key > max_l) and 
####  &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;  &nbsp; &nbsp;  &nbsp; &nbsp;            (min_r is None or node.key < min_r))
    
####  &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;  min_key = min(remove_none([min_l, node.key, min_r]))
####  &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;  max_key = max(remove_none([max_l, node.key, max_r]))
    
####  &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;  print(node.key, min_key, max_key, is_bst_node)
        
####  &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;  return is_bst_node, min_key, max_key

---

## Insertion in BST
#### Using the BST-property to perform insertion efficiently:
- Starting from the root node, compare the key to be inserted with the current node’s key
- If the key is smaller, recursively insert it in the left subtree (if it exists) or attach it as as the  left child if no left subtree exists.
- If the key is larger, recursively insert it in the right subtree (if it exists) or attach it as as the right child if no right subtree exists.


![](https://www.codesdope.com/staticroot/images/ds/bst8.png)












