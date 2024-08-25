### How are [[Iterables]] different to [[Iterators]]?
 Well, you can think of an iterable as a CONTAINER while iterators are the MECHANISM for going through that container. An iterable is like a box of items, holding all the elements that can be iterated over. On the other hand, an iterator is like a robotic arm that reaches into the box, picking up one item at a time and keeping track of its position. The iterable (container) can be used multiple times, creating a new iterator (robotic arm) each time you want to go through its contents. 

### Why do we use these?
This separation allows for efficient memory use and the ability to work with large or even infinite sequences.

### Iterable vs Iterator Comparison Table

| Aspect        | Iterable                               | Iterator                                     |
| ------------- | -------------------------------------- | -------------------------------------------- |
| Definition    | Container that can be iterated over    | Object that defines how to iterate           |
| Analogy       | A box of items                         | A robotic arm picking items from the box     |
| Purpose       | Holds a collection of data             | Traverses the collection one item at a time  |
| Reusability   | Can be iterated over multiple times    | Typically exhausted after one full iteration |
| In Python     | Implements `__iter__()`                | Implements `__iter__()` and `__next__()`     |
| Usage Example | `for item in my_list:`                 | `item = next(my_iterator)`                   |
| Common Types  | Lists, strings, dictionaries, sets     | Objects returned by `iter()`, generators     |
| State         | Doesn't keep track of iteration state  | Maintains current position in iteration      |
| Memory Usage  | May hold all items in memory           | Usually only stores current state            |
| Creation      | Often built-in types or custom classes | Created from an iterable                     |
