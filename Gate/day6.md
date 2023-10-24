* Learn about deadlock detection for multiple instance, ways to avoid deadlock, some numericals on max value of n so that no deadlock & types of locks(spinlock, livelock, deadlock)
* Solved array question (Print the longest length of the subarray having the targetted sum)
  - ```py def longestSubarrayWithSumK(a: [int], k: int) -> int:
    # Write your code here
    left=0
    current_sum=0
    max_len=0
    for right in range(len(a)):
        current_sum+=a[right]
        
        while current_sum>k:
            current_sum-=a[left]
            left+=1
        
        if current_sum==k:
            max_len=max(max_len,right-left+1)
            
    return max_len
    ```
  - The use of two pointer is best, if found targetted sum, right-left +1 , +1 because 0 based indexing
