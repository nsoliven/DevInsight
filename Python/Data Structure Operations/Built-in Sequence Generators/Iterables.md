## What is an Iterable?

An iterable in Python is like a container of items that you can go through one by one. Think of it as a box of toys where you can take out one toy at a time.

## Key Ideas

1. **Container**: An iterable holds multiple items.
2. **Can be looped over**: You can use a for loop to go through its items.
3. **Gives an iterator**: When asked, an iterable provides an iterator to go through its items.
4. **Reusable**: Unlike iterators, you can loop over an iterable multiple times.

## Common Iterables in Python

1. Lists: `[1, 2, 3]`
2. Strings: `"hello"`
3. Tuples: `(1, 2, 3)`
4. Dictionaries: `{"a": 1, "b": 2}`
5. Sets: `{1, 2, 3}`
6. Files (when opened)

## In Python Code

Here's how this looks in Python:

```python
# Lists are iterables
my_list = [1, 2, 3, 4, 5]  # This is our "toy box"

# We can loop through it
for item in my_list:  # Python creates an iterator for us behind the scenes
    print(item)

# Strings are also iterables
my_string = "hello"
for char in my_string:
    print(char)

# Dictionaries are iterables (looping gives keys by default)
my_dict = {"a": 1, "b": 2, "c": 3}
for key in my_dict:
    print(key, my_dict[key])
```

## Creating Your Own Iterable

You can create your own iterable by defining a class with an `__iter__()` method:

```python
class CountByTwo:
    def __init__(self, limit):
        self.limit = limit
        self.value = 0

    def __iter__(self):
        self.value = 0  # Reset for new iteration
        return self

    def __next__(self):
        if self.value >= self.limit:
            raise StopIteration
        self.value += 2
        return self.value

# Using our custom iterable
numbers = CountByTwo(10)
for num in numbers:
    print(num)  # Outputs: 2, 4, 6, 8, 10

# We can use it again
for num in numbers:
    print(num)  # Outputs: 2, 4, 6, 8, 10 again
```

## Why Use Iterables?

1. **Consistency**: They work with Python's for loops and many functions.
2. **Readability**: Makes your code easier to understand.
3. **Flexibility**: Can represent different types of data collections.

