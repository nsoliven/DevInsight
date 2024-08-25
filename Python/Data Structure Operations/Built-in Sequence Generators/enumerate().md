Creates an iterator of index-value pairs from an iterable.

```python
fruits = ['apple', 'banana', 'cherry']
for index, fruit in enumerate(fruits):
    print(f"{index}: {fruit}")
# Output:
# 0: apple
# 1: banana
# 2: cherry
```

Key points:
- Adds a counter to an iterable
- Useful for getting index alongside values in loops
- Returns an enumerate object (iterator)


Common characteristics:
- All are lazy (generate values on-demand)
- Return iterators, not lists
- Memory-efficient, especially for large sequences
- Built-in Python functions (no import needed)