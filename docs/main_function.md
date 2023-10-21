---
description: "Learn how to handle with the Main Function"
title: "Main Function Handling"
ms.date: 05/11/2023
ms.topic: "conceptual"
author: fejo-git
ms.reviewer: ---
---

## Main Function

### code example

```cpp
int main(int argc, const char *argv[]) {
for(int i = 0; i < argc; i++) {
        std::cout << argv[i] << std::endl;
}
std::cout << argv[0] << std::endl;
std::cout << argc << std::endl;

return 0;
}

```

`int main`: The main function is the entry point of a C/C++ program and it returns an integer. By convention, returning 0 usually indicates a successful execution, while a non-zero value can be used to indicate an error.

`int argc`: This parameter represents the number of command-line arguments passed to the program, including the name of the program itself.

`const char \*argv[]`: This parameter is an array of C-strings (character pointers), where each element in the array corresponds to a command-line argument. argv[0] typically contains the name of the program, and subsequent elements contain the actual command-line arguments provided when running the program.

### See also

- **[functions](../docs/functions.md)**
- **[iterations](../docs/iterations.md)**
- **[statements](../docs/statements.md)**
- **[Home](../README.md)**
