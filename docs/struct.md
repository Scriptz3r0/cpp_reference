---
description: "Learn how to handle with Struct"
title: "Struct Handling"
ms.date: 19/11/2023
ms.topic: "conceptual"
author: fejo-git
ms.reviewer: ---
---

## Struct

### what is struct

- Structs are available in both C and C++. In C++, structs are very similar to classes, but with some differences in their default access specifiers.
- In C++, structs have public access by default, whereas classes have private access by default. However, you can still specify access specifiers (public, - private, protected) in a C++ struct.
- In C++, you can create methods (member functions) in both classes and structs.
- Structs are often used to bundle related data together, while classes are used to bundle both data and methods.
- Structs are sometimes used to define lightweight data structures, and they are appropriate when you need to group a few related variables together, particularly when it's used within a single function.

So, while structs are similar to classes in C++, they are typically used for simpler data structures with public access by default, and they can include methods. However, whether you choose a struct or a class depends on your specific requirements and design choices.

### code example

```cpp
struct Student {
    string name;
    int age;
};

int main() {
std::vector<Student> students;
Student s = readStudent();
students.push_back(s);
}

```

### See also

- **[this vs c.property](../docs/this_vs_c.property.md)**
- **[encapsulation](../docs/encapsulation.md)**
- **[desctructor](../docs/destructor.md)**
- **[object oriented](../docs/object_oriented.md)**
- **[Home](../README.md)**
