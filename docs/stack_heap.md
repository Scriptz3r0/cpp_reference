---
description: "Learn how to handle with Stack and Heap"
title: "Stack and Heap Handling"
ms.date: 05/11/2023
ms.topic: "conceptual"
author: fejo-git
ms.reviewer: ---
---

## Stack and Heap

### stack

- Not arbitrarily large
- Store variables
- Automatically managed by C++

### heap

- For larger data sets
- Vector automatically resides in the heap

### array on heap

```cpp
int *a = new int[10] ();

```

Your statements describe some fundamental concepts in C++ memory management:

- `*a = Pointer`: This indicates the declaration of a pointer variable `a`. Pointers are variables that store memory addresses, allowing you to access data indirectly.

- `new = Heap`: `new` is an operator in C++ used to allocate memory on the heap. The heap is a region of memory that is typically used for dynamic memory allocation. Memory allocated with `new` persists until it is explicitly deallocated with `delete`, and if you don't deallocate it, it can lead to memory leaks.

- `() = Initialization with 0`: In C++, when you use `new` to allocate memory for an object, parentheses `()` are used to initialize the object. If you don't provide an explicit initializer, built-in types like `int` will be initialized to 0, while user-defined types will have their default constructors called.

You also mentioned:

- Stack is limited to a few megabytes: Yes, the stack is a region of memory used for function call management and local variable storage. Its size is typically limited, and excessive stack usage can lead to a stack overflow.

- Heap is not automatically deleted (memory leak): Correct, memory allocated on the heap is not automatically freed; you need to explicitly deallocate it using `delete`. Failure to do so can result in memory leaks, where allocated memory is not released and remains unavailable for other parts of your program.

These concepts are important for understanding memory management in C++ and ensuring efficient and safe memory usage.

```cpp
delete[]a;

```

To delete memory allocated on the heap in C++, you should use the delete operator. If you have a pointer variable a pointing to memory allocated on the heap, you can delete it as follows

### vector on heap

```cpp
std::vector<int> a = {1,2,3,4,5,6,7};

```

The variable name 'a' is located on the stack, while the values 1-7 are located on the heap.

### See also

- **[pointer](../docs/pointer.md)**
- **[pointer vs. reference](../docs/pointer_vs_reference.md)**
- **[vector](../docs/vector.md)**
- **[Home](../README.md)**
