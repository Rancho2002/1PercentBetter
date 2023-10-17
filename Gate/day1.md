* learn about bankers algorithm
* give a test on OS
* Solved one array question (Two Sum)
  - ```
    class Solution:
    def twoSum(self, nums: List[int], target: int) -> List[int]:
        d={}
        for i in range(len(nums)):
            more=target-nums[i]
            if more in d:
                return [i,d[more]]
        
            d[nums[i]]=i
    ```
* [free time] work with community (discord,linkedin)
