### Summary
When we analyze an algorithm, we determine its [[Time Complexity]] to understand how it performs. This helps us predict the efficiency and suitability for different tasks.

We analyze an algorithms Time Complexity using [[Asymptotic Notation]] based on their performance as input sizes grow in the with an Upper Bound, Lower Bound, Exact Bound and etc. This classification helps compare and choose the best algorithm for a given problem. 

### How to analyze an algorithm
We can start off analyzing an algorithm by breaking it into different parts.

Lets look at a function written in python as an example.
```python
def find_max(arr):
    if len(arr) == 0:
        return None
    
    max_value = arr[0]
    for num in arr[1:]:
        if num > max_value:
            max_value = num
    
    return max_value
```

We can see that part that will "grow" with input size is the array. We are iterating through the array with the for loop.

We can apply [[Big O Notation]] here, and see in the worst, average, and best case we will have to iterate through the whole array, thus we have $O(n)$ time, where n is the size of the algorithm. This is [[Linear Growth]]. 
