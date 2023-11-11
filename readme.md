# A list of high frequency algorithm questions for Google interveiws in 2003
## Tree
1. [2458. Height of Binary Tree After Subtree Removal Queries](https://leetcode.com/problems/height-of-binary-tree-after-subtree-removal-queries)  
  The idea is for a node, the max depth without that code is either from left or right subtree. So have two hash maps, key is node val, one hash map is to store the max depth without a code when performing preorder traversal from left, the other is for max depth without the node when performing preorder traversal from right. When doing preorder traversal from left, assign the max depth to the node, and then if current depth is larger than max depth, then update max depth. Then traverse left subtreee and right subtree.

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

## Heap
1. [2458. Height of Binary Tree After Subtree Removal Queries](https://leetcode.com/problems/height-of-binary-tree-after-subtree-removal-queries)  
  Key observation is that when multiple rooms are available, the room with smallest index should be picked so good candidate for a min heap. And when there is no room available, a meeting should be delayed until another meeting finishes, so good idea to use another mean heap.  
  1. The idea is to sort meetings based on start time and end time, then do a linear scan of the meetings. 
  1. For a start time, release all the meetings that have finished, i.e. finish time <= start time. Then if there are free meeting rooms, pick the room with the smallest index, and push to the heap of ending time and room index
  1. Else means no room is free, so the meeting need to be delayed. Pick a meeting that finishes earlist to get the new start time and free room. Push the expected end time and room to the heap.

    <details>
  
      ```python
    def mostBooked(self, n: int, meetings: List[List[int]]) -> int:
        freeRooms = [r for r in range(n)]
        busyRooms = []
        result = [0] * n
        for start, end in sorted(meetings):
            while busyRooms and busyRooms[0][0] <= start:
                endTime, room = heapq.heappop(busyRooms)
                heapq.heappush(freeRooms, room)
            
            if freeRooms:
                room = heapq.heappop(freeRooms)
                heapq.heappush(busyRooms, [end, room])
            else:
                endTime, room = heapq.heappop(busyRooms)
                heapq.heappush(busyRooms, [endTime + end - start, room])
            result[room] += 1
               
        return result.index(max(result))
      ```
    </details>
