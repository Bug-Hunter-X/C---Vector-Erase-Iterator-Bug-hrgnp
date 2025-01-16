# C++ Vector Erase Iterator Bug
This repository demonstrates a common bug in C++ when erasing elements from a `std::vector` while iterating using an index-based approach.  The provided code attempts to remove the element with value 5. However, the method employed leads to incorrect results due to index shifting after erasure.
The `bug.cpp` file contains the buggy code.  The solution is presented in `bugSolution.cpp`, showcasing a safer way to remove elements from a vector.
## Bug Description
When an element is removed using `vec.erase()`, the subsequent elements shift their indices. Therefore, when the loop continues, the next index might skip over an element or point to the wrong one. This can lead to unexpected behavior and incomplete removal of elements.
## Solution
The correct approach is to iterate using iterators and use the `erase` method with iterators.