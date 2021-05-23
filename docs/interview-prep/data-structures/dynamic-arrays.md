# Dynamic Arrays

> All problems in computer science can be solved by another level of indirection

## Definition and Implementation
Abstract data type with the following operations
- get(i): returns element at location i
  ```python
  if i < 0 or i >= size:
    ERROR: index out of range
  return arr[i]
  ```
- set(i, val): sets element i to val
  ```python
  if i < 0 or i >= size:
    ERROR: index out of range
  arr[i] = val
  ```
- push(val): adds val to the end
  ```python
  if size == capacity:
    allocate new_arr[2 x capacity]
    for i from 0 to size - 1:
      new_arr[i] = arr[i]
    free arr
    arr = new_arr
    capacity = 2 x capacity
  arr[size] = val
  size = size++
  ```
- remove(i): removes element at location i
  ```python
  if i < 0 or i >= size:
    ERROR: index out of range
  for j from i to size - 2:
    arr[j] = arr[j+1]
  size = size-1
  ```
- size(): returns the number of elements
  ```python
  return size
  ```

#### Store
- arr: dynamically-allocated array
- capacity: size of the dynamically-allocated array
- size: number of elements currently in the array
  
#### Examples
- c++: vector
- java: ArrayList
- python: list (all are this type)

#### Runtimes
- get(i): O(1)
- set(i, val): O(1)
- push(val): O(n)
- remove(i): O(n)
- size: O(1)


# Summary
- Unlike static arrays, dynamic arrays can be resized
- Appending a new element to a dynamic array is often constant time, but can take O(n)
- Some space is wasted
