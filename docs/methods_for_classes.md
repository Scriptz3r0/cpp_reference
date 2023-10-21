---
description: "Learn how to Handle with more Methods for Classes"
title: "Methods for Classes Handling"
ms.date: 19/11/2023
ms.topic: "conceptual"
author: fejo-git
ms.reviewer: ---
---

## Methods for Classes

### string

```cpp
string s ("Hallo Welt");

```

```cpp
class Car{
public:
    string name;
    int age;
    Car(string name, int age) : name(name), age(age) {

    }
};

```

### copyconstructor

- C++ automatically generates a copy constructor.
- When explicitly defining the constructor, modifications can be made.
- Set the copy constructor to private to ensure that variables must be passed by reference.

```cpp
Car(Car &other) {
    this->name = other.name;
}

```

### See also

- **[object oriented](../docs/object_oriented.md)**
- **[methods for classes](../docs/methods_for_classes.md)**
- **[destructor](../docs/destructor.md)**
- **[Home](../README.md)**
