* Learn about memory management module in OS, it includes memory allocation, memory deallocation, protection
* fixed partition contiguous memory management technique, some partition allocation policy(first fit, best fit, worst fit, next fit)
* fragmentation
* solved one array question Buy and Sell stock
    -
  ```py
  class Solution:
    def maxProfit(self, prices: List[int]) -> int:
        mintoBuy=float("inf")
        maxProf=0
        for i in range(len(prices)):
            if prices[i]<mintoBuy:
                mintoBuy=prices[i]
            prof=prices[i]-mintoBuy
            maxProf=max(prof,maxProf)
        return maxProf
  ```
  * Catch is we will buy the minimum and sell at the maximum. To track maximum, we use max func.
    
