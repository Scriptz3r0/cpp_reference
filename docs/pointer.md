---
description: "Learn how to handle with Pointers"
title: "Pointer Handling"
ms.date: 05/11/2023
ms.topic: "conceptual"
author: fejo-git
ms.reviewer: ---
---

## Pointer

### general Information

```cpp
&a; // local address of a

int *b = &a; // Pointer at a Integer

*b; // value of the address

```

### pointer with array (c-array)

```cpp
int a[3] = {1, 2, 3};

std::cout << a << std::endl;          // address 1
std::cout << a + 1 << std::endl;      // address 2
std::cout << a + 2 << std::endl;      // address 3

std::cout << *(a + 2) << std::endl;   // value of address 3

```

### array with pointer as function parameter

```cpp
void doSomething(int *a, int size) {
 std::cout << *a << std::endl;
}
```

or

```cpp
void doSomething(int *a, int size) {
 for(int i = 0; i < size; i++) {
        std::cout << a[i] << std::endl;
 }
}

```

### See also

- **[pointer vs. reference](../docs/pointer_vs_reference.md)**
- **[stack heap](../docs/stack_heap.md)**
- **[functions](../docs/functions.md)**
- **[Home](../README.md)**
