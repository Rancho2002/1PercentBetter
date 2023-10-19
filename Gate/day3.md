* Solved this question on array (Majority element)
  - ```
    class Solution:
    def majorityElement(self, nums: List[int]) -> int:
        count:int=0
        element:int=nums[0]

        for i in range(len(nums)):
            if count==0:
                element=nums[i]
            if element==nums[i]:
                count+=1
            else:
                count-=1
        return element
    ```
    <strong>Trick here is if count==0 is separate case, element ==nums[I] is separate , both can't came in same if block</strong>
