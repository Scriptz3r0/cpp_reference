---
description: "Learn how to handle with Iterators"
title: "Iterators Handling"
ms.date: 05/11/2023
ms.topic: "conceptual"
author: fejo-git
ms.reviewer: ---
---

## Iterators

### definition

```cpp
std::vector<string>::iterator i = names.begin();

```

The iterator is positioned at the beginning.

```cpp
names.begin();

```

The iterator is positioned at the end.

```cpp
names.end();

```

### iterator with vector

```cpp
for(std::vector<string>::iterator i = names.begin(); i < names.end(); i++) {
        std::cout << *i << std::endl;
}

```

An alternative and more common method.

```cpp
for(const auto &name : names) {
    std::cout << " - " << name << std::endl;
}
```

### compare iterators (storage)

```cpp
std::vector<string>::iterator j = names.begin();
std::vector<string>::iterator i = names.end();
i--;
std::cout << (j < i) << std::endl;

// output 1

```

### See also

- **[vectors](../docs/vector.md)**
- **[vector advanced handling](../docs/vector_advanced_handling.md)**
- **[important commands](../docs/important_commands.md)**
- **[Home](../README.md)**
