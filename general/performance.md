# Performance Tips

Write efficient code that runs faster and uses fewer resources.

---

## Choose the Right Data Structures

Use sets, dictionaries/maps, or hash tables for fast lookups instead of lists/arrays.

```python
# Fast lookup
if item in my_set:
```
## Avoid Repeating Work
Don’t repeat the same calculations or logic inside loops. Store results when possible.

## Use Built-in Functions
Standard library methods are often faster than custom code.

```js
// Faster
array.includes(x)
```
## Reduce Nesting and Looping
Nested loops slow things down. Flatten logic or use smarter structures.

## Profile Before Optimizing
Use profiling tools to find the real bottlenecks. Don’t guess.

```python
import timeit
timeit.timeit("sum(range(1000))", number=1000)
```
## Process Data in Chunks
When dealing with large files or streams, process them in parts to save memory.

```python
for line in open("file.txt"):
    handle(line)
```
This should help your code run faster!
