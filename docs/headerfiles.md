---
description: "Learn how to handle with Headerfiles"
title: "Headerfiles Handling"
ms.date: 05/11/2023
ms.topic: "conceptual"
author: fejo-git
ms.reviewer: ---
---

## Headerfiles

### Problem

Let's say we have two C++ files, a.cpp and b.cpp, and they cyclically depend on each other for compilation.

### Solution

We create a.cpp and b.cpp, along with a.h and b.h files. During compilation, a.cpp references b.h, and b.cpp references a.h.

### Create a header file

1. Create a file named HeaderFile.h.

2. Use the same name as the .cpp file with methods.

```cpp
#pragma once

#include <vector>
#include <string>
#include <sstream>

class TicTacToeField {

private:
 Sstd::vector<std::vector<int>> field;

public:
 TicTacToeField();
 int calcualteWinner();
 std::string getFieldStr();
};

```

### Create a cpp file

1. Create a file named HeaderFile.cpp.

2. Use the same name as the .h file with methods.

```cpp
#include <vector>
#include <string>
#include <sstream>
#include <iostream>

#include "TicTacToeField.h"

using namespace std;

TicTacToeField::TicTacToeField() {
 // Code
 }
string TicTacToeField::getFieldStr() {
 // Code
}

```

### See also

- **[main function](../docs/main_function.md)**
- **[standard library](../docs/standard_library_overview.md)**
- **[pragma once](../docs/pramga_once_preprocessor_directives.md)**
- **[Home](../README.md)**
