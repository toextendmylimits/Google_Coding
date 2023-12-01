# These questions appear in the past 6 months, so could appear again
|Question                 | Category        | Frequency as on 1 Dec | Dates           | Practice Again | Note          |
| ----------------------  | -------------   | ----------------------| --------------- | -------------  | ------------- | 
|[359. Logger Rate Limiter](https://leetcode.com/problems/logger-rate-limiter)   | Hashmap| 23 | 01/12 | YES | Practice approach with hash set plus queue
|[2101. Detonate the Maximum Bombs](https://leetcode.com/problems/detonate-the-maximum-bombs) | Graph BFS/DFS| 22 | 01/12 | YES | Should memorize both DFS and BFS. Never use continue in a if not inside loop. Often should use return in a function. TC O(N^3), SC O(N^2)
|[2458. Height of Binary Tree After Subtree Removal Queries](https://leetcode.com/problems/height-of-binary-tree-after-subtree-removal-queries)    | Tree DFS | 20 | 01/12 | YES | Very difficult. Practice a few more times
|[1110. Delete Nodes And Return Forest](https://leetcode.com/problems/delete-nodes-and-return-forest) | Tree DFS | 16| 01/12 | YES | Need to maintain whether a node is deleted and whether its parent is deleted. Practice a few more times
|[2402. Meeting Rooms III](https://leetcode.com/problems/meeting-rooms-iii)| Tree DFS | 15 | 01/12 | YES | a. Need to sort meetings. b. Use heap for free rooms. Don't forget to heapify. c. Also use heap for time when a busy room is free again. d. use hash map to record a room's meetings
|[4. Median of Two Sorted Arrays](https://leetcode.com/problems/median-of-two-sorted-arrays)| Binary Search | 14 | 01/12 | YES | Need to memorize
|[56. Merge Intervals](https://leetcode.com/problems/merge-intervals) | Merge Intervals | 12| 01/12 | NO | Very familiar. Just have a quick look
|[2265. Count Nodes Equal to Average of Subtree](https://leetcode.com/problems/count-nodes-equal-to-average-of-subtree) | Tree DFS | 9 | 01/12 | YES | Return count of nodes total sum in each recursion call 
|[253. Meeting Rooms II](https://leetcode.com/problems/meeting-rooms-ii) | Sweep Line | 11 | 01/12 | YES | Remember to sort hash map items
|[2713. Maximum Strictly Increasing Cells in a Matrix](https://leetcode.com/problems/maximum-strictly-increasing-cells-in-a-matrix)| Dynamic programming | 9 | 01/12 | YES | Use hash map to store num and its positions. Sort hash map ascendingly. Also record max sequence that can reach an item in a row or column
|[366. Find Leaves of Binary Tree](https://leetcode.com/problems/find-leaves-of-binary-tree)    | Tree DFS | 6 | 01/12 | YES | Beware height starts from 1
|[2007. Find Original Array From Doubled Array](https://leetcode.com/problems/find-original-array-from-doubled-array) | Greedy | 6 | 01/12 | YES | Use hash map to store num and frequency. Sort hash map keys ascendingly. Beware special case 0
|[939. Minimum Area Rectangle](https://leetcode.com/problems/minimum-area-rectangle) | Greedy | 6 | 01/12 | YES | Use hash map to store all points for easy look up. Pick pair of points that could be points on the diagonal, and check the other two points
|[2437. Number of Valid Clock Times](https://leetcode.com/problems/number-of-valid-clock-times) | Not clear | 6 | 01/12 | YES | Have 3 functions for format, match, and count. Need to practice again
|[2013. Detect Squares](https://leetcode.com/problems/detect-squares)| Greedy | 4 | 01/12 | YES | Use hash map to store all points and its count. Pick pair of points that could be points on the diagonal, and check the other two points
|[226. Invert Binary Tree](https://leetcode.com/problems/invert-binary-tree)     | Tree DFS/BFS | 4 | 01/12 | YES | Easy but beware BFS as well
|[100. Same Tree](https://leetcode.com/problems/same-tree)     | Tree DFS/BFS | 4 | 01/12 | YES | Beware to check left against left and right against right. This is not isMirror
|[111. Minimum Depth of Binary Tree](https://leetcode.com/problems/minimum-depth-of-binary-tree)     | Tree DFS/BFS | 2 | 01/12 | YES | Practice DFS for Depth and Height
|[54. Spiral Matrix](https://leetcode.com/problems/spiral-matrix)| Matrix | 4 | 01/12 | YES |
|[143. Reorder List](https://leetcode.com/problems/reorder-list) | Linked List | 2 | 1/12 | YES | Find middle, reverse second half, then connect. In while loop, check second half's next not null
|[759. Employee Free Time](https://leetcode.com/problems/employee-free-time) | 3 | Merge Intervals | 12| 01/12 | NO | Very familiar. Beware the sorting critieria
|[57. Insert Interval](https://leetcode.com/problems/insert-interval)| 7| Merge Intervals | 12| 01/12 | NO | Relatively clear. Practice if there is time


