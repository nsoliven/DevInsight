Combines multiple iterables into an iterator of tuples.

```python
names = ['Alice', 'Bob', 'Charlie']
ages = [25, 30, 35]
for name, age in zip(names, ages):
    print(f"{name} is {age} years old")
# Output:
# Alice is 25 years old
# Bob is 30 years old
# Charlie is 35 years old
```

Key points:
- Pairs elements from two or more iterables
- Stops at the length of the shortest iterable
- Returns a zip object (iterator)
- Useful for parallel iteration