https://leetcode.com/submissions/#/1

Language: Java; Brute force approach; TC=O(n^2); MC=O(n)

code:


class Solution {
    public int[] twoSum(int[] nums, int target) {
        for(int i = 0; i < nums.length; i++){
            for(int j = i+1; j < nums.length; j++){
                int total = target - nums[i];
                
                if(total == nums[j]){
                    return new int[] {i, j};
                }
            }
        }
        throw new IllegalArgumentException("no match found");
    }
}