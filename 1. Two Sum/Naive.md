# 💡 The Solution 

```python
def two_sum(nums, target):
    # Iterate through the list of numbers
    for i in range(len(nums)):
        for j in range(i + 1, len(nums)):
            # Check if the current pair of numbers adds up to the target
            if nums[i] + nums[j] == target:
                return [i, j]  # Return the indices of the two numbers

    # If no solution is found, return an empty list or raise an exception
    return []
```

# 🔍 The Explanation 

[![1. Two Sum](http://img.youtube.com/vi/KLlXCFG5TnA/0.jpg)](http://www.youtube.com/watch?v=KLlXCFG5TnA "YouTube Link")

# 📜 Summary 
The provided Python code solves the Two Sum problem using a brute-force approach. It iterates through the list of numbers, checking all possible pairs to see if their sum equals the target. If a pair with the desired sum is found, it returns a list containing the indices of those two numbers. If no solution is found, it returns an empty list or raises an exception. This approach has a time complexity of O(n^2) due to the nested loops.

# 📚 Topics Used 
- Nested Loops
- List Iteration
- Conditional Statements
