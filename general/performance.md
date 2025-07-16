# Performance Tips

## Use the Right Data Structures

Choosing the correct data structure can drastically improve performance.

Example:
```python
# Slower
if item in my_list:  # O(n)
```
```python
# Faster
if item in my_set:   # O(1)
```
Use:
set for fast membership checks
dict for key-value lookups
deque for fast inserts/removals at both ends

## Avoid Repeating Expensive Operations
Don't repeat calculations inside loops. Cache the result if it's reused.

Bad:

```python
for user in users:
    if calculate_score(user) > 10:
        ...
```
Better:

```python
for user in users:
    score = calculate_score(user)
    if score > 10:
        ...
```
## Use Built-in Functions and Libraries
Python’s built-ins are written in C and are often faster than custom solutions.

Instead of:

```python
total = 0
for x in numbers:
    total += x
```
Use:

```python
total = sum(numbers)
```
Also explore modules like itertools, collections, and functools for efficient tools.

## Minimize Loops and Nesting
Avoid nested loops when possible. Flatten logic or use smarter data structures.

Example:

```python
# Bad: O(n^2)
for a in A:
    for b in B:
        if a == b: ...
```
```python
# Better: O(n)
b_set = set(B)
for a in A:
    if a in b_set: ...
```
## Profile Before Optimizing
- Don’t guess what’s slow — measure it. Use profiling tools:
- timeit for timing small code snippets
- cProfile for analyzing larger programs
- Your IDE’s performance tools (e.g., PyCharm Profiler)

Example:
```python
import timeit
print(timeit.timeit("sum(range(1000))", number=1000))
```
## Process Large Data in Chunks
If you're working with large files or datasets, load/process them in chunks instead of all at once.


```python
# Reading large files
with open("big.txt") as f:
    for line in f:
        process(line)
```
This avoids memory overload and improves performance on low-resource machines.
