# Important ones to memorize

## Two Pointers 
|Question                 | Dates           | Practice Again | Note          |
| ----------------------  |  ---------------| -------------  | ------------- | 
|[80. Remove Duplicates from Sorted Array II](https://leetcode.com/problems/remove-duplicates-from-sorted-array-ii) | 25/11 | YES | Still difficult, practice two approaches
|[1099 two Sum less than k](https://leetcode.com/problems/two-sum-less-than-k) | 2511 | YES | Remember to sort, and also update with result = max(result, total). result = total wouldn't necessairly
|[259. 3 Sum Smaller](https://leetcode.com/problems/3sum-smaller)| 25/11 | YES | Sort. Update result += right - left
[16. 3 Sum Closet](https://leetcode.com/problems/3sum-closest)  | 25/11 | YES | Not 100% clear, need to save diff = curr_sum - target
|[151. Reverse Words in a String](https://leetcode.com/problems/reverse-words-in-a-string) | 25/11 | YES | Don't forget to check curr word again after end of loop. 
|[285. Move Zeroes](https://leetcode.com/problems/move-zeroes)  | 25/11 | YES | Find first zero idx, if not exist, return. Then swap zero with non-zero element and increase zero index
|[67. Add Binary](https://leetcode.com/problems/add-binary)| 25/11 | YES | Beware to reverse if using array to stor result, and use str() to convert digit of array |

## Tree DFS/BFS
|Question                 | Dates           | Practice Again | Note          |
| ----------------------  |  ---------------| -------------  | ------------- | 
|[109. Convert Sorted List to Binary Search Tree](https://leetcode.com/problems/convert-sorted-list-to-binary-search-tree) | 25/11 | YES | Simulate inorder traversal. Difficult, need to not only code it but more importantly to explain it clearly
|[112. Path Sum](https://leetcode.com/problems/path-sum) | 25/11 | YES | Practice BFS more
|[129. Sum Root to Leaf Numbers](https://leetcode.com/problems/sum-root-to-leaf-numbers) | 25/11 | YES | Need even more clear
|[543. Diameter of Binary Tree](https://leetcode.com/problems/diameter-of-binary-tree)  | 25/11 | YES | Calculate height recursively. Practice more
|[1522. Diameter of N-Ary Tree](https://leetcode.com/problems/diameter-of-n-ary-tree)  | 25/11 | YES | Tricky, need to two largest height in each step
[235. Lowest Common Ancestor of a Binary Search Tree](https://leetcode.com/problems/lowest-common-ancestor-of-a-binary-search-tree)| 25/11 | YES | If root is > both, go left; < both, go right; else return root
|[236. Lowest Common Ancestor of a Binary Tree](https://leetcode.com/problems/lowest-common-ancestor-of-a-binary-tree) | 25/11 | YES | Need to memorize
[1644. Lowest Common Ancestor of a Binary Tree II](https://leetcode.com/problems/lowest-common-ancestor-of-a-binary-tree-ii) | 25/11 | YES | Need to memorize
|[114. Flatten Binary Tree to Linked List](https://leetcode.com/problems/flatten-binary-tree-to-linked-list) | 26/11 | YES | Not clear at all, Need to memorize
|[491. Non-decreasing Subsequences](https://leetcode.com/problems/non-decreasing-subsequences) | 26/11 | YES | Not clear at all, got it wrong again. Need to memorize
|[131. Palindrome Partitioning](https://leetcode.com/problems/palindrome-partitioning) | 26/11 | YES | Better still practice more
|[17. Letter Combinations of a Phone Number](https://leetcode.com/problems/letter-combinations-of-a-phone-number)  | 26/11 | YES | Very clear but can practice more if there is time
|[22. Generate Parentheses](https://leetcode.com/problems/generate-parentheses/) | 26/11 | YES | Very clear but can practice more if there is time and should focus on explaining the thought process
|[113. Path Sum II](https://leetcode.com/problems/path-sum-ii) | 26/11 | YES | Not 100% clear
|[47. Permutations II](https://leetcode.com/problems/permutations-ii/)| 26/11 | YES | Still difficult
|[90. Subsets II](https://leetcode.com/problems/subsets-ii)| 26/11 | YES | Memorize how to avoid duplicates
|[40. Combination Sum II](https://leetcode.com/problems/combination-sum-ii)| 26/11 | YES | Not 100% clear, need to memorize
|[39. Combination Sum](https://leetcode.com/problems/combination-sum) )| 26/11 | YES | Not 100% clear, need to memorize
|[216. Combination Sum III](https://leetcode.com/problems/combination-sum-iii)| 26/11 | YES | Not 100% clear, need to memorize
|[1254. Number of Closed Islands](https://leetcode.com/problems/number-of-closed-islands)| 28/11 | YES | Not 100% clear, need to memorize
[130. Surrounded Regions](https://leetcode.com/problems/surrounded-regions)  | 28/11 | YES | Not 100% clear, need to memorize
|[79. Word Search](https://leetcode.com/problems/word-search)   | 28/11 | YES | Not clear, need to memorize
|[286. Walls and Gates](https://leetcode.com/problems/walls-and-gates) | 28/11 | YES | Not 100% clear, need to memorize
|[752. Open the Lock](https://leetcode.com/problems/open-the-lock)  | 28/11 | YES | Not 100% clear, need to memorize. Return turns when checking popped element
|[127. Word Ladder](https://leetcode.com/problems/word-ladder) | 28/11 | YES | Not 100% clear, need to memorize. Return 0 in the end
|[124. Binary Tree Maximum Path Sum](https://leetcode.com/problems/binary-tree-maximum-path-sum) | 28/11 | YES | Not clear at all, need to memorize, and explain. 4 cases for max sum that pass a node
|[297. Serialize and Deserialize Binary Tree](https://leetcode.com/problems/serialize-and-deserialize-binary-tree)| 28/11 | YES | Not clear, must memorize
|[1136. Parallel Courses](https://leetcode.com/problems/parallel-courses) | 28/11 | YES | Beware mistake of fogretting to initialize indegree if it's a hash map

## Binary Search
|Question                 | Dates           | Practice Again | Note          |
| ----------------------  |  ---------------| -------------  | ------------- | 
|[153. Find Minimum in Rotated Sorted Array](https://leetcode.com/problems/find-minimum-in-rotated-sorted-array)| 29/11 | YES | Forgot how to do it. Should compare with last element. Practice again.
|[1011. Capacity To Ship Packages Within D Days](https://leetcode.com/problems/capacity-to-ship-packages-within-d-days)| 29/11 | YES | Practice again to be more familiar. Record the total weight that can be shipped on a single day and reset it if an extra day is needed
|[4. Median of Two Sorted Arrays](https://leetcode.com/problems/median-of-two-sorted-arrays)| 29/11 | YES | Very difficult. Need to memorize a few times
|[1146. Snapshot Array](https://leetcode.com/problems/snapshot-array)| 29/11 | YES | Very difficult. Need to memorize a few times

## Prefix sum
|Question                 | Dates           | Practice Again | Note          |
| ----------------------  |  ---------------| -------------  | ------------- | 
|[560. Subarray Sum Equals K](https://leetcode.com/problems/subarray-sum-equals-k) | 29/11 | YES | Practice again if there is time
|[523. Continuous Subarray Sum](https://leetcode.com/problems/continuous-subarray-sum) | 29/11 | YES | Got it wrong. Practice again.
|[528. Random Pick with Weight](https://leetcode.com/problems/random-pick-with-weight)| 29/11 | YES | Got it wrong. random_num < prefix_sum[mid]
|[238. Product of Array Except Self](https://leetcode.com/problems/product-of-array-except-self)| 29/11 | YES | Need to be more familiar

## Linked List
|Question                 | Dates           | Practice Again | Note          |
| ----------------------  |  ---------------| -------------  | ------------- | 
|[146. LRU Cache](https://leetcode.com/problems/lru-cache)  | 29/11 | YES | More practice if there is time. Never forget self when reference own method
|[1650. Lowest Common Ancestor of a Binary Tree III](https://leetcode.com/problems/lowest-common-ancestor-of-a-binary-tree-iii)| 29/11 | YES | High-frequency for facebook
|[206. Reverse Linked List](https://leetcode.com/problems/reverse-linked-list) )| 29/11 | YES | Got it wrong. Set prev first then set curr
|[238. Product of Array Except Self](https://leetcode.com/problems/product-of-array-except-self)| 29/11 | YES | Need to be more familiar
|[143. Reorder List](https://leetcode.com/problems/reorder-list)| 30/11 | YES | Very difficult. Memorize the code. When reording, check while second_half and second_half.nex

## Dynamic programming
|Question                 | Dates           | Practice Again | Note          |
| ----------------------  |  ---------------| -------------  | ------------- | 
|[62. Unique Paths](https://leetcode.com/problems/unique-paths)  | 30/11 | YES | Look again to be very familiar
|[70. Climbing Stairs](https://leetcode.com/problems/climbing-stairs) | 30/11 | YES | Look again to be very familiar
| [322. Coin Change](https://leetcode.com/problems/coin-change) | 30/11 | YES | Initialize dp[0] = 0 otherwise float("inf"). Need to memorize it
|[198. House Robber](https://leetcode.com/problems/house-robber)| 30/11 | YES | Not clear. Practice more
|[5. Longest Palindromic Substring](https://leetcode.com/problems/longest-palindromic-substring)| 30/11 | YES | Expend from center or dynamic programming. Need to practice more
|[647. Palindromic Substrings](https://leetcode.com/problems/palindromic-substrings)| 30/11 | YES | Expend from center or dynamic programming. Need to practice more
|[516. Longest Palindromic Subsequence](https://leetcode.com/problems/longest-palindromic-subsequence) | 30/11 | YES | Dynamic programming. Need to practice more
|[1216. Valid Palindrome III](https://leetcode.com/problems/valid-palindrome-iii)| 30/11 | YES | Dynamic programming. Need to practice more
[2713. Maximum Strictly Increasing Cells in a Matrix](https://leetcode.com/problems/maximum-strictly-increasing-cells-in-a-matrix)| 30/11 | YES | Very difficult, need to practice more






