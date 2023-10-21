---
description: "Learn how to handle with Encapsulation"
title: "Encapsulation Handling"
ms.date: 05/11/2023
ms.topic: "conceptual"
author: fejo-git
ms.reviewer: ---
---

## Encapsulation

### Code Example

The class Cat inherits the properties of the class Animal and adds the name.

```cpp
class Animal {
public:
 double weight;
 int legs;
};

class Cat:public Animal {
public:
 std::string name;
}
```

### Protected, Public and Private

- `private`: Accessible only from within the class itself.
- `protected`: Accessible from within the class itself and from derived classes.
- `public`: Accessible from anywhere, including outside the class.

### Parent Method

Using an underscore at the end of variable names in `private` can be a useful convention to distinguish class member variables from other identifiers, but it's not a strict rule. It's a matter of coding style and can vary depending on the coding standards of the project or the personal preferences of the developer. Some coding guidelines do recommend this convention to make it clear that a variable is a class member, but it's not universally followed. The most important thing is to be consistent within your codebase.

```cpp
std::string TicTacToeGame::getFieldStr() {
 stringstream result;
 result << "Player1: " << player1 << std::endl;
 result << "Player2: " << player2 << std::endl;

 result << TicTacToeField::getFieldStr();
 return result.str();
}

```

### See also

- **[this vs c.property](../docs/this_vs_c.property.md)**
- **[overloaded constructor](../docs/overload_cunstructor.md)**
- **[desctructor](../docs/destructor.md)**
- **[object oriented](../docs/object_oriented.md)**
- **[Home](../README.md)**
