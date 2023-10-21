---
description: "Learn how to Handle Const Methods"
title: "Const Methods Handling"
ms.date: 19/1012023
ms.topic: "conceptual"
author: fejo-git
ms.reviewer: ---
---

## Const Methods

### code example

`a.getPs()` can be passed to a function.

```cpp
class Auto {
public:
    int ps;
    int getPs() const {
            return this->ps;}
};

```

### const method as function parameter

Pass `a.getPs()` to a function.

```cpp
void doSomething(const Auto &a) {
    std::cout << "Auto: " << a.getPs() << " PS " << std::endl;
}

```

### See also

- **[functions](../docs/functions.md)**
- **[virtual methods](../docs/virtual_methods.md)**
- **[](../docs/main_function.md)**
- **[Home](../README.md)**
