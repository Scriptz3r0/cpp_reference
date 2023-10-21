---
description: "Learn how to handle with iterations"
title: "Iteration Handling"
ms.date: 19/11/2023
ms.topic: "conceptual"
author: fejo-git
ms.reviewer: ---
---

## Iterations

### for-statement

The FOR loop iterates through the loop for a specific predefined number of times. It consists of an initial value, a termination condition, and an increment. The FOR loop is condition-controlled.

```cpp
for (int i = 0; i < 10; i++) {
    std::cout << i << " ";
}

// output: 1 2 3 4 5 6 7 8 9

```

In the code example: The initial value of i is 0. The condition is i < 10, and i is incremented by 1 with each iteration. Therefore, during each iteration starting from 0, a value is printed, and after printing, i is incremented by 1. Thus, we have an output from 0 to 9.

### while-statement

The WHILE loop continues to execute until a specific condition is met. The WHILE loop is also condition-controlled.

```cpp
int i = 0;
while(i < 10) {

    std::cout << i << " ";
    i++;

}

// output: 0 1 2 3 4 5 6 7 8 9

```

In the code example: The initial value of i is 0. The condition is i < 10, and i is incremented by 1 with each iteration. Therefore, during each iteration starting from 0, the value of i is printed, and after printing, i is incremented by 1. Thus, we have an output from 0 to 9.

### do-while-statement

The DO-WHILE loop is foot-controlled, ensuring that the loop is executed at least once. The DO-WHILE loop continues to execute until a specific condition is met.

```cpp
int i = 0;
do {

    std::cout << i << " ";
    i++;

} while(i < 10);

// output: 0 1 2 3 4 5 6 7 8 9

```

In the code example: The initial value of i is 0. The condition is i < 10, and i is incremented by 1 with each iteration. Consequently, during each iteration, starting from 0, the value of i is printed, and after the output, i is incremented by 1. This results in an output from 0 to 9.

### See also

- **[Statements](../docs/statements.md)**
- **[Functions](../docs/functions.md)**
- **[Home](../README.md)**
