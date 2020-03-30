# 1. Two Sum

https://leetcode.com/problems/two-sum/


Given an array of integers, return indices of the two numbers such that they add up to a specific target.

You may assume that each input would have exactly one solution, and you may not use the same element twice.

```
Example:

Given nums = [2, 7, 11, 15], target = 9,

Because nums[0] + nums[1] = 2 + 7 = 9,
return [0, 1].
```


### My Thought: 
have a hashmap with key as the target and try to find the remaining number in the rest of the list


### Code: 
```java
class Solution {
    public int[] twoSum(int[] nums, int target) {
        HashMap<Integer, Integer> map = new HashMap<Integer, Integer>(); 
        int[] result = new int[2]; 

        for(int i=0; i<nums.length; i++){
            if(map.containsKey(target-nums[i])){
                result[0]=i;
                result[1]=map.get(target-nums[i]); 
                break; 
            }
            else {
                map.put(nums[i],i); 
            }
        }
        return result; 
    }
}
```    


## Solution
https://blog.csdn.net/crystal6918/article/details/66971861


