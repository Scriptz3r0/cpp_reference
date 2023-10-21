---
description: "Learn how to handle with Arrays"
title: "Array Handling"
ms.date: 24/10/2023
ms.topic: "conceptual"
author: fejo-git
ms.reviewer: ---
---

## Arrays

### array description

An array allows you to group multiple variables of the same data type together. You access elements in an array using an index. When defining an array, you need to specify the data type and the size (number of elements) of the array.

### syntax

Initialization of an array with the data type Integer, a size of 4 (index from 0 to 3), and the name "numbers."

During initialization, the array can also be directly populated with values like this: {1, 3, 5, 7}.

```cpp

#include <array>

array <int, 4> numbers;
array <int, 4> numbers = {1,3,5,7};

```

### handle with an arrays

```cpp

numbers[3] = 9;

```

Storage location 3 is assigned the value 9 in the array. This means that the element at index 3 in the array "numbers" now holds the value 9.

```cpp

std::cout << numbers[4];

```

It's important to note that in many programming languages, including C++, array indices typically start at 0, so there is no storage location 4 in an array with a size of 4 (indices 0 to 3). If you attempt to access the element at index 4, you may encounter an "out of bounds" error, as it would be beyond the bounds of the array.

### size of an array

```cpp

numbers.size();

```

Returns the size of the array as the return value.

### output of all elements of an array

```cpp

for(int i = 0; i < numbers.size(); i++) {

 std::cout << numbers[i] << std::endl;
}

```

or

```cpp

for(const int &value : numbers) {

 std::cout << value << std::endl;
}

```

In both FOR loops, you iterate through all values until the size of the array is reached.

### multidimensional arrays

```cpp

array<array<int,2>, 3> a = {{
 {1,2},
 {3,4},
 {5,6}
}};

```

Initialization of the two-dimensional array 'a' with preset values.

```cpp

std::cout << a [0][0] << std::endl;

```

Output of a two-dimensional array.

### array as a parameter into a function

```cpp

int calculatewinner(const array<array<int,3>,3> &field);

```

The array is passed by reference, allowing you to work with the original values. However, the use of 'const' before the array prevents the values from being overwritten.

### See also

- **[function](../docs/functions.md)**
- **[vector](../docs/vector.md)**
- **[vector-advanced-handling](../docs/vector_advanced_handling.md)**
- **[Home](../README.md)**
