---
description: "Learn the Difference between a List and Vector"
title: "List and Vector Handling"
ms.date: 05/11/2023
ms.topic: "conceptual"
author: fejo-git
ms.reviewer: ---
---

## List and Vector

### vector

Random-Access Memory:

| 11 | 12 | 13 | 14 | 15 |

### list

Random-Access Memory:

| 11 | → | 12 | → | 13 | → | 14 | → | 15 |

- A list stores data in a different structure.
- The individual elements are linked together.
- Therefore, values can be inserted at any time, and these values are stored somewhere in memory, with only the connections being adjusted.

### difference

| vector                                                    | list                                               |
| --------------------------------------------------------- | -------------------------------------------------- |
| Is used when data is added at the end.                    | Is used when data needs to be inserted in between. |
| --------------------------------------------------------- | -------------------------------------------------- |
| Runs more efficiently as memory locations are contiguous. | When two lists need to be merged together.         |
| --------------------------------------------------------- | -------------------------------------------------- |

### code-example (list)

```cpp
#include <list>
#include <iostream>

int main () {
    std::list<int> a ={1, 2, 3, 4, 5,};
    std::list<int> b ={6, 7, 8};

    a.splice(a.end(), b);

    for(auto const &value : a) {
        std::cout<< value << std::endl;
    }

// output: 1 2 3 4 5 6 7 8
}

```

### See also

- **[vector](../docs/vector.md)**
- **[vector advanced handling](../docs/vector_advanced_handling.md)**
- **[standard library](../docs/standard_library_overview.md)**
- **[Home](../README.md)**
