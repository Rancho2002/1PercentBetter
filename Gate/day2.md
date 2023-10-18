* Learn about deadlock avoidance
* Solved one array problem (Sort colors)
     ```
     class Solution:
        def swap(self,arr,i,j):
            arr[i],arr[j]=arr[j],arr[i]
    
        def sortColors(self, arr: List[int]) -> None:
            """
            Do not return anything, modify nums in-place instead.
            """
            low=0
            mid=0
            high=len(arr)-1
            while mid<=high:
                if arr[mid]==0:
                    self.swap(arr,low,mid)
                    low+=1
                    mid+=1
                elif arr[mid]==1:
                    mid+=1
                else:
                    self.swap(arr,mid,high)
                    high-=1
     ```
  <strong>Learnings here: Mid is incremented in two cases only i.e for arr[mid]=2 only high decremented</strong>
