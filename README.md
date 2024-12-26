# Unexpected Behavior Modifying std::vector via Raw Pointer

This repository demonstrates a common, yet subtle, error in C++ when working with `std::vector` and raw pointers. The code attempts to modify the contents of a `std::vector` using a raw pointer obtained via `&vec[0]`. However, this approach is unsafe because `std::vector` may reallocate its internal memory during operations like `push_back()`, invalidating the pointer. This can lead to undefined behavior and unexpected results.

The `bug.cpp` file contains the erroneous code, while `bugSolution.cpp` shows a safer and more idiomatic way to achieve the intended modification using iterators or direct element access.

## How to reproduce
1. Clone this repository.
2. Compile and run the code using a C++ compiler (e.g., g++).