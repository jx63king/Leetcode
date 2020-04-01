# 53. Maximum Subarray 

https://leetcode.com/problems/maximum-subarray/


Given an integer array nums, find the contiguous subarray (containing at least one number) which has the largest sum and return its sum.

```
Example:
Input: [-2,1,-3,4,-1,2,1,-5,4],
Output: 6
Explanation: [4,-1,2,1] has the largest sum = 6.
```

### Follow up:
If you have figured out the O(n) solution, try coding another solution using the divide and conquer approach, which is more subtle.


### My thoughts: 
having two pointers, making sure that the right pointer index is bigger or equal to the left one
sum up until find the largetst one 


### Code: 
```java
class Solution {
    public int maxSubArray(int[] nums) {
        if(nums.length == 0) return 0; 

        int sum = nums[0]; 
        int max = nums[0]; 
        int i=1; 
        
        while(i<nums.length) {
            if(sum <= 0) {
                sum = nums[i]; 
            }
            else {
                sum = sum + nums[i]; 
            }

            // get the bigger one
            if(sum>max) {
                max = sum; 
            }
            i++; 
        }
        return max; 
    }

}
```

### Notes: 
Sum, Max 

## Solution
https://blog.csdn.net/liusf1993/article/details/87910479
