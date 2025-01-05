# std::vector<bool> Gotcha

This repository demonstrates a common issue encountered when using `std::vector<bool>` in C++.  `std::vector<bool>` is specially implemented as a bitset for memory efficiency. However, this specialization deviates from the standard vector interface and can lead to unexpected behavior and performance problems.

The `bug.cpp` file shows an example where operations on `std::vector<bool>` fail to match expectations.

`bugSolution.cpp` provides solutions to demonstrate how to mitigate these issues.

**Note:**  For most applications where you need an array-like structure of booleans, using `std::vector<char>` (or `std::vector<uint8_t>`) is recommended for better compatibility with algorithms and clearer semantics.