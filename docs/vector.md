---
description: "Learn how to handle with Vectors"
title: "Vector Handling"
ms.date: 24/10/2023
ms.topic: "conceptual"
author: fejo-git
ms.reviewer: ---
---

## Vectors

### vector description

A vector is a dynamic array. Unlike static arrays, vectors do not have a fixed size and can dynamically adjust to accommodate the number of elements.

### syntax

```cpp

#include <vector>

std::vector<string> data;
std::vector<string> data = {"Max", "Eva"};

```

A vector of type string named 'data' initialized with 'Max' and 'Eva'.

### append or delete a element within a vector

```cpp

data.push_back("123");

```

To append "123" to the 'data' vector, use the push_back method.

```cpp

data.pop_back();

```

To remove the last element from the vector 'data', you can use the pop_back method.

### output of all elements within a vector

```cpp

for(const &element : data) {

    std::cout << element << std::endl;
}

```

All elements from the 'data' vector are printed. By using the '&' symbol, we work with the original values, but due to 'const,' they cannot be modified.

### access the first memory location of a vector

```cpp

std::cout << data[0] << std::endl;

```

Using `data[x]`, you can access any memory block by substituting the desired index 'x.'

Caution: It's possible to access memory blocks outside the bounds of the vector, which can lead to unintended consequences or errors.

or

```cpp

std::cout << data.at(0) << std::endl;

```

Using `data.at(x)`, you can access any memory block by substituting the desired index 'x'. However, it also checks whether the specified memory block is within the vector. If it's not, the program will terminate. (This also works for arrays.)

or

```cpp

std::cout << data.front() << endl;

```

All three commands (codes) only output the first memory block of the vector.

### access the last memory location of a vector

```cpp

std::cout << data[data.size() - 1] << std::endl;

```

Here, the last memory block is accessed by determining the size of the vector using `size()` and then subtracting 1 because we start with memory block 0.

or

```cpp

std::cout << data.back() << endl;

```

Here, the last memory block is automatically accessed and printed.

### function with multidimensional vector

```cpp

bool is_magic(const std::vector <vector<int>> &ma) {
 int sum = 0;
 for(int i = 0; i < ma.at(0).size();i++) {
  sum += ma.at(0).at(i);
 }
 for(const std::vector<int> &m : ma) {
   int sum2 = 0;
   for(int j : m) {
    sim2 += j;
   }
   if(sum2 != sum) {
    return false;
   }
   else {
    return true;
   }
 }
}

```

### See also

- **[vector-advanced-handling](../docs/vector_advanced_handling.md)**
- **[list](../docs/list_vs_vector.md)**
- **[datatypes](../docs/datatypes.md)**
- **[Home](../README.md)**
