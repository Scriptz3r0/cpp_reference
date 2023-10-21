---
description: "Learn how to handle with Pointers and References"
title: "Pointer and Reference Handling"
ms.date: 05/11/2023
ms.topic: "conceptual"
author: fejo-git
ms.reviewer: ---
---

## Pointer vs Reference

### code example

```cpp
#include <iostream>
#include <vector>

void withPointer(int *p, int size) {
    p++;
    std::cout << *p << std::endl;
    std::cout << p << std::endl;        //Adresse
}

void withReference(const std::vector<int> &r) {
    for(int element : r) {
            std::cout << element << std::endl;
    }
}

int main() {
const int P_LENGTH = 4;
int p[P_LENGTH] = {15, 16, 17, 18};
withPointer(p, P_LENGTH);

std::vector<int> r = {15, 16, 17, 18};
withReference(r);
return 0;
}

```

### See also

- **[pointer](../docs/pointer.md)**
- **[iterators](../docs/iterators.md)**
- **[standard library](../docs/standard_library_overview.md)**
- **[Home](../README.md)**
