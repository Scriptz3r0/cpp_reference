---
description: "Learn how to Handle with Pragma Once and Preprocessor Directives"
title: "Pragma Once and Preprocessor Directives Handling"
ms.date: 19/11/2023
ms.topic: "conceptual"
author: fejo-git
ms.reviewer: ---
---

## Pragma Once and Preprocessor Directives

### pragma once

This command is for mac users

```bash
g++ -E "Pfad der Datei" >~/Desktop/datei.cpp

```

`##pragma once` ensures that the header files are included only once and not with every invocation of the functions.

### preprocessor directive (makro)

```cpp
#define Some_Value 200

std::cout << Some_Value << endl;

```

"In the translated code"

```cpp
std::cout << 200 << std::endl;

```

### request makro

"If not defined yet, assign the value 200 to SomeValue."

```cpp
#ifndef SomeValue
#define SomeValue 200
#endif

```

### option to pragma once

```cpp
#ifndef SomeFunctions.h
#define SomeFunctions.h
Programm (main)
#endif

```

### See also

- **[headerfiles](../docs/headerfiles.md)**
- **[main function](../docs/main_function.md)**
- **[important commands](../docs/important_commands.md)**
- **[Home](../README.md)**
