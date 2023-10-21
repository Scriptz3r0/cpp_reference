---
description: "Learn how to handle with an Overloaded Constructor"
title: "Overloaded Cunstructor Handling"
ms.date: 05/11/2023
ms.topic: "conceptual"
author: fejo-git
ms.reviewer: ---
---

## Overloaded Constructor

### Code Example

normal constructor

```cpp
TicTacToeField();

```

overloaded constructor

```cpp
TicTacToeField(std::vector<std::vector<int>> field);

```

implemented overloaded constructor

```cpp
TicTacToeField::TicTacTieField(std::vector<std::vector<int>> field) {
    this->field = field;
    std::cout << "I am the constructor that receives the 'field' variable as an argument." << std::endl;
}

```

constructor call in main function

```cpp
TicTacToeField f(field);

```

### See also

- **[this vs c.property](../docs/this_vs_c.property.md)**
- **[encapsulation](../docs/encapsulation.md)**
- **[desctructor](../docs/destructor.md)**
- **[object oriented](../docs/object_oriented.md)**
- **[Home](../README.md)**
