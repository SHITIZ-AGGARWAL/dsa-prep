# majority-element

Given an array nums of size n, return the majority element.
The majority element is the element that appears more than ⌊n / 2⌋ times. You may assume that the majority element always exists in the array.

### Solution One : Space Optimised
#### Space Complexity : O(1)
#### Time Complexity  : O(n^2)
```
class Solution {
    public int majorityElement(int[] nums) {
        
        int max = nums.length/2;

        for (int num : nums) 
        {
            int count = 0;
            for (int ele : nums) 
            {
                if (ele == num) 
                {
                    count += 1;
                }
            }

            if (count > max) {
                return num;
            }

        }

        return -1;    
    }
}
```
### Solution Two : Best

