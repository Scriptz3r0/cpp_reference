---
description: "Learn how to handle with statements"
title: "Statement Handling"
ms.date: 19/11/2023
ms.topic: "conceptual"
author: fejo-git
ms.reviewer: ---
---

## Iterations

### if-statement

The IF statement is used to execute a program segment based on a specified condition.

```cpp
int a = 0;

if(a < 2) {

    std::cout << "a is less than 2" << std::endl;

}


// output: a is less than 2

```

In the code example: We have the variable 'a' assigned a value of 0. In the IF condition, it checks whether 'a' is less than 2. When this condition is met, as it is in this example, you will receive the output that "a is less than 2."

### if-else-statement

The IF-ELSE statement is used to execute one program segment if a condition is met and another program segment if the condition is not met.

```cpp
int a = 0;
int b = 2;

if(a < b) {

    std::cout << "a is less than b" << std::endl;

}

else {

    std::cout << "b is less than or equal to a" << std::endl;

}

// output: a is less than 2

```

In the code example: We have the variable 'a' assigned a value of 0 and the variable 'b' assigned a value of 2. In the IF condition, it checks whether 'a' is less than 2. When this condition is met, as it is in this example, you will receive the output "a is less than 2." If this condition is not met, the ELSE statement is automatically executed, and you will get the output "b is less than or equal to a."

### else-if-statement

The ELSE-IF statement is used to execute one program segment if a condition is met, or another program segment if a different condition is met. The ELSE-IF condition is checked only if the preceding IF statement is not satisfied.

```cpp
int a = 0;
int b = 2;

if(a < b) {

    std::cout << "a is less than b" << std::endl;

}

else if(a > b) {

    std::cout << "a is greater than b" << std::endl;

}

else {

    std::cout << "b is equal to a" << std::endl;

}

// output: a is less than 2

```

In the code example: We have the variable 'a' assigned a value of 0 and the variable 'b' assigned a value of 2. In the IF condition, it checks whether 'a' is less than 2. When this condition is met, as it is in this example, you will receive the output "a is less than 2." If this condition is not met, the ELSE statement is automatically executed, and you will get the output "b is less than or equal to a." The ELSE-IF statement is not used in this example.

### Ternary Operator

```cpp
int age1 = 28;
int age2 = 56;

int older_age = age1 > age2 ? age1 : age2

// Bool EXPR ? TRUE Rückgabe : FALSE Rückgabe

```

### See also

- **[Statements](../docs/statements.md)**
- **[Functions](../docs/functions.md)**
- **[Home](../README.md)**
