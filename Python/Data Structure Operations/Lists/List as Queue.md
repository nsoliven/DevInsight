### Implementation
```python
from collections import deque
queue = deque([])
queue.append(1)     # Enqueue
queue.append(2)
front_element = queue.popleft()  # Dequeue
```