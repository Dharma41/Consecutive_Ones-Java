# Consecutive_Ones-Java
Given a binary array nums, return the maximum number of consecutive 1's in the array.     Example 1:  Input: nums = [1,1,0,1,1,1] Output: 3 Explanation: The first two digits or the last three digits are consecutive 1s. The maximum number of consecutive 1s is 3.


# Intuition
<!-- Describe your first thoughts on how to solve this problem. -->

# Approach
<!-- Describe your approach to solving the problem. -->

# Complexity
- Time complexity:
<!-- Add your time complexity here, e.g. $$O(n)$$ -->
O(n) -> It will traverse the array once

- Space complexity:
<!-- Add your space complexity here, e.g. $$O(n)$$ -->
O(1)

# Code
```
class Solution {
    public int findMaxConsecutiveOnes(int[] nums) {
        int count=0;
        int sum=0;
        for(int i=0;i<nums.length;i++){
            if(nums[i]==1){
                count++;

            }else{
                // sum = Math.max(sum,count);
                sum=sum>count?sum:count;
                count=0;
            }
        }
        // sum = Math.max(sum,count);
        sum=sum>count?sum:count;
        return sum;
        
    }
}
```
