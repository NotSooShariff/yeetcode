# The solution

```python
def removeElement(nums,val):
    # Initialize k to count the valid elements
    k = 0
    # Iterate through the list of numbers
    for i in range(len(nums)):
        # Check if the index at nums[i] does not equal to val
        if nums[i] != val:
            # Copy the current valid element at position 'i' to the next valid position 'k'
            nums[k] = nums[i]
            # Increment the count of valid elements 'k' by 1
            k += 1
    # Return the count of valid elements, which represents the new length of the modified list
    return k    
```

# 🔍 The Explanation 

[![27. Remove Element](http://img.youtube.com/vi/Pcd1ii9P9ZI/0.jpg)](https://www.youtube.com/watch?v=Pcd1ii9P9ZI "YouTube Link")

# 📜 Summary 
The provided Python code solves the Remove Element problem using a two-pointer approach. Iterates through the array only once, copying valid elements to their new positions, and maintaining a count of valid elements using the 'k' pointer. This approach has a time complexity of O(n) due to iterating through the loop once.

# 🔑 Prerequisite Knowledge 
- List Iteration
- Conditional Statements

