* Learn about wait-flow-graph to check deadlock for single instance
* Solved the array question Maximum Subarray
    
  ```
  class Solution:
    def maxSubArray(self, nums: List[int]) -> int:
        sum=0
        maxi=float("-inf")
        for i in nums:
            sum=sum+i
            if maxi<sum:
                maxi=sum
            if sum<0:
                sum=0
        return maxi
  ```
<strong>take maxi as int min because it can be -10^4</strong>
