---
description: "Learn how to handle with C-Strings"
title: "C-String Handling"
ms.date: 05/11/2023
ms.topic: "conceptual"
author: fejo-git
ms.reviewer: ---
---

## C-String

In C, there wasn't a convenient data type like "string." Instead, strings were often represented as arrays of characters.

### problem

In C, you can't directly pass arrays to functions; instead, you pass them as pointers. Additionally, you would typically need to pass the length of the array separately or a pointer to the end of the array to indicate its boundaries. This is because C does not store the size of the array within the array itself, and functions need this information to work with arrays effectively.

To pass a C-string (array) to a function in C, you typically need to pass multiple parameters.

### solution

- At the end of the string, there is a '\0' character.
- The function knows that when it is passed a pointer, it should output the string until the '\0' character is encountered.

### code-example

```cpp
#include <iostream>
#include <cstring>

void doSomething(char *name) {
 std::cout << name << std::endl;
 std::cout << strlen(name) << std::endl;
}

int main() {
char name[12] = "Max";
doSomething(name);
}

```

### output with printf

```cpp
string name(”Hallo Welt”, 10);

```

It reads 10 characters (even if a '\0' character is encountered after the 2nd character).

```cpp
string name = “Hallo Welt”;

```

Read until '\0' is encountered.

```cpp
printf("Ich habe gesagt: %s", a.c_str());

```

### See also

- **[string](../docs/string.md)**
- **[stringstream](../docs/stringstream.md)**
- **[standard library](../docs/standard_library_overview.md)**
- **[Home](../README.md)**
