# 💡 The Solution 

```python
class Solution(object):
    def twoSum(self, nums, target):
        # Create an empty dictionary to store previously seen numbers and their indices
        prevMap = {} 

        # Loop through the input list 'nums' using 'enumerate'
        # 'enumerate' provides both the index and the value of each element in 'nums'
        for index, currentnumber in enumerate(nums):
            # Calculate the difference between the 'target' and the current number
            difference = target - currentnumber

            # Check if the 'difference' (complement) is already in the 'prevMap' dictionary
            if difference in prevMap:
                # If it is, it means that we've found two numbers whose sum equals the 'target'
                # Return a list containing the indices of those two numbers
                return [prevMap[difference], index]

            # If the 'difference' is not in 'prevMap', add the current number to 'prevMap'
            # The key is the current number, and the value is its index
            prevMap[currentnumber] = index
```

# 🔍 The Explanation 

[![1. Two Sum](http://img.youtube.com/vi/KLlXCFG5TnA/0.jpg)](http://www.youtube.com/watch?v=KLlXCFG5TnA "1. Two Sum")

# 📜 Summary 
The provided Python code solves the Two Sum problem using a dictionary to efficiently store previously seen numbers and their indices. It iterates through the input list `nums`, calculates the difference between the `target` and the current number, and checks if the difference (complement) is in the dictionary. If found, it returns a list of indices of the two numbers that add up to the target. If not found, it continues iterating. This approach avoids redundant iterations and has a time complexity of O(n).

# 📚 Topics Used 
- Dictionary (Hashmap)
- Enumeration (`enumerate`)
- Looping and Conditional Statements
- Data Structures and Algorithms
- Problem Solving

