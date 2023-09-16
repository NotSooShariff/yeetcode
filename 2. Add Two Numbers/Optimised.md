
# 💡 The Solution 

```python
class Solution:
    def addTwoNumbers(self, l1: ListNode, l2: ListNode) -> ListNode:
        # Create a dummy head node to simplify list manipulation
        dummyHead = ListNode(0)
        tail = dummyHead  # Initialize a tail pointer for building the result list
        carry = 0  # Initialize a carry variable for handling carry values

        # Loop until both input lists and the carry are exhausted
        while l1 is not None or l2 is not None or carry != 0:
            # Get the digits from the input lists (default to 0 if None)
            digit1 = l1.val if l1 is not None else 0
            digit2 = l2.val if l2 is not None else 0

            # Calculate the sum of digits along with the carry
            sum = digit1 + digit2 + carry
            digit = sum % 10  # Calculate the current digit
            carry = sum // 10  # Calculate the carry for the next iteration

            # Create a new node with the current digit
            newNode = ListNode(digit)

            # Connect the new node to the result list
            tail.next = newNode
            tail = tail.next  # Move the tail pointer to the new node

            # Move to the next nodes in the input lists if available
            l1 = l1.next if l1 is not None else None
            l2 = l2.next if l2 is not None else None

        result = dummyHead.next  # The actual result starts from the next node of dummyHead
        dummyHead.next = None  # Disconnect the dummyHead from the result list
        return result  # Return the resulting linked list
```

# 🔍 The Explanation 

[![2. Add Two Numbers](http://img.youtube.com/vi/wgFPrzTjm7s/0.jpg)](http://www.youtube.com/watch?v=wgFPrzTjm7s "2. Add Two Numbers")

# 📜 Summary 
The provided Python code adds two numbers represented as linked lists. It uses a dummy head node and a tail pointer to construct the result list while handling carry values during addition. The code iterates through the input lists, calculates the sum of corresponding digits, updates the carry, and constructs the result linked list. The algorithm handles edge cases where input lists may have different lengths or carry extends beyond the lists.

# 📚 Topics Used 
- Linked Lists
- Node Manipulation
- Arithmetic Operations
- Looping and Conditional Statements
- Problem Solving
