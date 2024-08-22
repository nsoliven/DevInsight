## Summary
In Python, a `set` is an unordered collection of unique elements, similar to the `unordered_set` in C++. However, there are some key differences:

- Python sets are implemented using hash tables with open addressing.
- C++ `unordered_set` typically uses separate chaining for collision resolution.

Both use hashing in the background, providing fast O(1) average-case time complexity for most operations.

## Basic Operations:

### Initialization
```python
# Creating an empty set
my_set = set()

# Creating a set with elements
fruits = {"apple", "banana", "orange"}

# Creating a set from a list (duplicates are removed)
numbers = set([1, 2, 2, 3, 4, 4, 5])
```

### Adding Elements
```python
fruits.add("grape")  # Add a single element
fruits.update(["kiwi", "mango"])  # Add multiple elements
```

### Removing Elements
```python
fruits.remove("banana")  # Raises KeyError if not found
fruits.discard("pear")   # Doesn't raise an error if not found
popped = fruits.pop()    # Remove and return an arbitrary element
fruits.clear()           # Remove all elements
```

### Membership Test
```python
if "apple" in fruits:
    print("We have apples!")
```

### Size
```python
fruit_count = len(fruits)
```

## Set Operations (Useful for LeetCode)

### Union
```python
set1 = {1, 2, 3}
set2 = {3, 4, 5}
union_set = set1 | set2  # or set1.union(set2)
```

### Intersection
```python
intersection_set = set1 & set2  # or set1.intersection(set2)
```

### Difference
```python
difference_set = set1 - set2  # or set1.difference(set2)
```

### Symmetric Difference
```python
symmetric_diff = set1 ^ set2  # or set1.symmetric_difference(set2)
```

### Subset and Superset
```python
is_subset = set1 <= set2  # or set1.issubset(set2)
is_superset = set1 >= set2  # or set1.issuperset(set2)
```

## Advanced Usage

### Set Comprehension
```python
even_squares = {x**2 for x in range(10) if x % 2 == 0}
```

### Frozen Sets (Immutable)
```python
immutable_set = frozenset([1, 2, 3])
```

### Iteration (Important for LeetCode)
```python
for item in my_set:
    print(item)

# Convert to list if order is needed
sorted_list = sorted(my_set)


# iterate through each item, remember index doesnt represent anything meaningful
for index, item in enumerate(my_set): 
	print(f"Item {index}: {item}")
```

## LeetCode-specific Operations

### Convert List to Set (Remove Duplicates)
```python
unique_elements = set(my_list)
```

### Find Common Elements
```python
common = set1.intersection(set2, set3)
```

### Count Unique Elements
```python
unique_count = len(set(my_list))
```

### Check for Disjoint Sets
```python
are_disjoint = set1.isdisjoint(set2)
```

### Update Set In-Place
```python
set1.update(set2)  # Adds elements from set2 to set1
```