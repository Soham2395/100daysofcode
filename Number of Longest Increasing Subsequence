class Solution:
    def findNumberOfLIS(self, nums: List[int]) -> int:
        dp = [1] * len(nums) 
        count = [1] * len(nums) 
        for i in range(len(nums)): 
            for j in range(i): 
                if nums[i] > nums[j]: 
                    if dp[j] >= dp[i]: 
                        dp[i] = dp[j] + 1  
                        count[i] = count[j]  
                    elif dp[j] + 1 == dp[i]:  
                        count[i] += count[j]  
        max_length = max(dp) 
        return sum(c for d, c in zip(dp, count) if d == max_length)
