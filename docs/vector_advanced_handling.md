---
description: "Learn how to handle with Vectors (Advanced)"
title: "Advanced Vector Handling"
ms.date: 05/11/2023
ms.topic: "conceptual"
author: fejo-git
ms.reviewer: ---
---

## Advanced Vector

### expand

"In the code example, I can insert numbers into vector 'a' using 'a.insert'. I specify the position first, by using 'a.begin() + 2' to move two positions forward, and then I want to insert 123."

```cpp
std::vector<int> a = {1, 2, 3, 4, 5};
a.insert(a.begin() + 2, 123);

// output: 1 2 123 3 4 5

```

### delete

In the code example, I delete the element in vector 'a' using 'a.erase' at the position from the beginning + 2 positions.

```cpp
std::vector<int> a = {1, 2, 3, 4, 5};
a.erase(a.begin() + 2);

// output: 1 2 4 5

```

### delete area

Caution! It can be costly in terms of performance with vectors, as other elements need to be shifted and copied when using 'a.erase' in this way.

```cpp
std::vector<int> a = {1, 2, 3, 4, 5};
a.erase(a.begin() + 1, a.end() -2);

// output: 1 4 5

```

### See also

- **[vector](../docs/vector.md)**
- **[list](../docs/list_vs_vector.md)**
- **[datatypes](../docs/datatypes.md)**
- **[Home](../README.md)**
