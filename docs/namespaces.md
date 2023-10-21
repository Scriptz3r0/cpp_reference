---
description: "Learn how to Handle with Namespaces"
title: "Namespaces Handling"
ms.date: 19/11/2023
ms.topic: "conceptual"
author: fejo-git
ms.reviewer: ---
---

## Namespaces

### definition

A program can be divided into namespaces to ensure variable names are uniquely named.

### code-example

A namespace for the class Car is created.

```cpp
namespace factory {
    class Car;
}

class factory::Car{
public:
    int age = 0;
    void drive();
};

```

Calling the drive method of the Car class with the namespace.

```cpp
void factory::Car::drive() {};

```

It's not always necessary to write `factory::` before `Car::drive()`.

```cpp
using namespace factory;

```

It's not always necessary to write `std::` before `cout`.

```cpp
using namespace std;

```

### See also

- **[object oriented](../docs/object_oriented.md)**
- **[pragma once preprocessor directives](../docs/pramga_once_preprocessor_directives.md)**
- **[standard library overview](../docs/standard_library_overview.md)**
- **[Home](../README.md)**
