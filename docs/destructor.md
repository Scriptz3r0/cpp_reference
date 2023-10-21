---
description: "Learn how to Handle with Desctructors"
title: "Destructor Handling"
ms.date: 19/11/2023
ms.topic: "conceptual"
author: fejo-git
ms.reviewer: ---
---

## Destructor

### definition

- Constructor: Upon creating the class
- Destructor: At the end

### code-example

```cpp
class Auto {
private:
int *a;
public:
Auto() {
    a = new int[10];
    std::cout << "Konstruktor!" << std::endl;
}
~Auto() {
    delete [] a;
    std::cout << "Destruktor!" << std::endl;
}
};
```

### See also

- **[object oriented](../docs/object_oriented.md)**
- **[encapsulation](../docs/encapsulation.md)**
- **[methods for classes](../docs/methods_for_classes.md)**
- **[Home](../README.md)**
