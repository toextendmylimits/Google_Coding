# A list of high frequency algorithm questions for Google interveiws in 2003
## Tree
1. [2458. Height of Binary Tree After Subtree Removal Queries](https://leetcode.com/problems/height-of-binary-tree-after-subtree-removal-queries)  
  The idea is for a node, the max depth without that code is either from left or right. So have two hash maps, key is node val, one hash map is to store the max depth without a code when performing preorder traversal from left, the other is for max depth without the node when performing preorder traversal from right. When doing preorder traversal from left, assign the max depth to the node, and then if current depth is larger than max depth, then update max depth. Then traverse left subtreee and right subtree.

    <details>
  
      ```python
     def treeQueries(self, root: Optional[TreeNode], queries: List[int]) -> List[int]:
          maxDepthLeft = 0
          maxDepthRight = 0
          nodeMaxDepthLeftMap = {}
          nodeMaxDepthRightMap = {}
          def preorderFromLeft(root, depth):
              nonlocal maxDepthLeft, nodeMaxDepthLeftMap
              if not root:
                  return
              nodeMaxDepthLeftMap[root.val] = maxDepthLeft
              maxDepthLeft = max(maxDepthLeft, depth)
              preorderFromLeft(root.left, depth + 1)
              preorderFromLeft(root.right, depth + 1)
          
          def preorderFromRight(root, depth):
              nonlocal maxDepthRight, nodeMaxDepthRightMap
              if not root:
                  return
              
              nodeMaxDepthRightMap[root.val] = maxDepthRight
              maxDepthRight = max(maxDepthRight, depth)
              preorderFromRight(root.right, depth + 1)
              preorderFromRight(root.left, depth + 1)
  
          preorderFromLeft(root, 0)
          preorderFromRight(root, 0)
  
          result = []
          for query in queries:
              result.append(max(nodeMaxDepthLeftMap[query], nodeMaxDepthRightMap[query]))
  
          return result
      ```
    </details>
