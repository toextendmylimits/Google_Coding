# Binary Search
1. [35. Search Insert Position](https://leetcode.com/problems/search-insert-position)  
    If the target is not in the array, then in the end left > right, and arr[right] < target < arr[left] so return left. Better use an example like (3, 7) to check how 2, 4, 9 works.  
    <details>

    ```python
        def searchInsert(self, nums: List[int], target: int) -> int:
        left = 0
        right = len(nums) - 1
        while left <= right:
            mid = left + (right - left) // 2
            if nums[mid] == target:
                return mid
            elif nums[mid] < target:
                left = mid + 1
            else:
                right = mid - 1
        return left
    ```
    </details>
1. [69. Sqrt(x)](https://leetcode.com/problems/sqrtx)  
    Beware edge case when n is 0 or n is less than 4.  
    <details>

    ```python
    def mySqrt(self, x: int) -> int:
        if x == 0:
            return 0
        if x < 4:
            return 1
        left = 2
        right = x
        result = -1
        while left <= right:
            mid = left + (right - left) // 2
            if mid <= x // mid:
                result = mid
                left = mid + 1
            else:
                right = mid - 1
        
        return result
    ```
    </details>
1. [34. Find First and Last Position of Element in Sorted Array](https://leetcode.com/problems/find-first-and-last-position-of-element-in-sorted-array)
1. [33. Search in Rotated Sorted Array](https://leetcode.com/problems/search-in-rotated-sorted-array)  
1. [540. Single Element in a Sorted Array](https://leetcode.com/problems/single-element-in-a-sorted-array) 
    Not that difficult, should think again
