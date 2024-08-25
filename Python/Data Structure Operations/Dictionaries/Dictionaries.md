## Summary
In python we have `dictionaries` as our main built-in data structure that serves as a [[Hash Map]] implementation. In C++, this would be the `unordered_map`'s alternative, but there are key differences.
- As of Python 3.7+, dictionaries preserve insertion order.
	- Python uses a Split-Table Approach
		- One table (array) stores the hash table, containing only keys and hashes.
		- Another table stores the actual key-value entries in the order they were inserted.
- You can rely on items being retrieved in the same order they were inserted.
## Basic Operations:
### Initialization
```python
# creating an empty dictionary
my_dictionary = {}

# creating a dictionary with key-value pairs
fruits = {"apple": 5, "banana": 3}
```
### Insertion and Update
- Use square brackets `[]` or the `update()` method
```python
fruits["orange"] = 7  # Add new key-value pair
fruits["apple"] = 6   # Update existing value
fruits.update({"grape": 4, "banana": 5})  # Add/update multiple pairs
```

### Access
- Use square brackets `[]` or the `get()` method
```python
apple_count = fruits["apple"]
orange_count = fruits.get("orange", 0)  # Returns 0 if key not found
```

### Removal
- `pop()`: Remove and return value
- `del`: Remove key-value pair
```python
banana_count = fruits.pop("banana")  # Removes and returns value
del fruits["apple"]  # Removes key-value pair
```

### Membership Test
- Use the `in` operator
```python
if "grape" in fruits:
    print("We have grapes!")
```

### Size
- `len()` function
```python
fruit_count = len(fruits)
```

## Advanced Operations

### Iteration
```python
# Iterate over keys
for fruit in fruits:
    print(fruit)

# Iterate over key-value pairs
for fruit, count in fruits.items():
    print(f"{fruit}: {count}")

# Get keys and values
all_fruits = fruits.keys()
all_counts = fruits.values()
```

### Dictionary Comprehension
```python
squared = {x: x**2 for x in range(5)}
```

### Merging Dictionaries
- In Python 3.9+:
```python
combined = fruits | {"kiwi": 2}
```
- In earlier versions:
```python
combined = {**fruits, **{"kiwi": 2}}
```
