---
description: "Learn how to handle with functions"
title: "Function Handling"
ms.date: 19/11/2023
ms.topic: "conceptual"
author: fejo-git
ms.reviewer: ---
---

## Functions

### Syntax and Call of a Function

```cpp

#include <iostream>

void doSomething(std::string name);        // function declaration

int main() {

    std::string name = "Test";
    doSomething(name);                     // function call
}

void doSomething(std::string name) {       // function definition

    std::cout << name << std::endl;

}

```

In this code, we have a function called `doSomething`. Before the main program, there is a function declaration, which is only necessary when the function definition appears after the main program. The function has a user-defined name. You can pass parameters to a function, and you can define a return value for it.

### Function without Parameters and without a Return Value

In the function, there is neither a return value nor any parameters. The "void" preceding the function indicates that there is no return value.

```cpp

#include <iostream>

void doSomething();

int main() {

    doSomething();
}

void doSomething( ) {

    std::cout << "This is a function without parameters and without a return value."
        << std::endl;

}

```

In the code example: In the main program, the function `doSomething()` is called. Subsequently, the program execution jumps into the function, where it carries out the output of the text. Afterward, we return to the main program.

### Function with Parameters and without a Return Value

In the function `doSomething()`, we now have a parameter of type String. This is indicated by the parameter, along with its type, within the function's parentheses.

```cpp

#include <iostream>

void doSomething(std::string name);

int main() {

    std::string name = "test";
    doSomething(name);
}

void doSomething(std::string name) {

    std::cout << name << std::endl;

}

In the code example: In the main program, a string variable is created and declared as "Test." Subsequently, the function call passes the parameter "name" to the `doSomething()` function, which then prints this parameter using `cout` in the console.

```

### Function without Parameters and with a Return Value

In the function `doSomething()`, we have a return value, as indicated by the "int" before the function. This means that the return value is an integer. The return value is always returned using the `return` statement.

```cpp

#include <iostream>

int doSomething();

int main() {

    std::cout << "sum = " << doSomething();
}

int doSomething( ) {

    return 2+2;

}

```

In the code example: The function `doSomething()` is called, it calculates the sum of 2+2, and then returns this sum to the main program. In the main program, this sum is then printed.

### Function with Parameters and with a Return Value

In the `doSomething()` function, we have a return value of type Integer and two parameters, both of type Integer.

```cpp

#include <iostream>

int doSomething(int a, int b);

int main() {

    int a = 2;
    int b = 4;

    std::cout << "sum: " << doSomething(a,b) << std::endl;
}

int doSomething(int a, int b) {

    return a + b;

}

```

In the code example: In the main program, two variables, 'a' and 'b,' are declared and assigned the values 2 and 4, respectively. Following this, there is an output that includes "Sum: " and the return value of the `doSomething(a, b)` function with parameters 'a' and 'b'. During this output, the program execution jumps into the function, calculates the sum of 'a' and 'b', and then returns it for display in the main program.

### Overloaded Functions

I can achieve function overloading by duplicating the function definition while altering only the data types. When an Integer parameter is passed to the function, it utilizes the Integer version, and when a parameter of type Double is provided, it employs the Double type version.

```cpp

int f (int x) {

    std::cout << "f(int x)" << endl;
    return x * x;
}

double f (double x) {

    std::cout << "f(double x)" << endl;
    return x * x;
}

```

### See also

- **[headerfiles](../docs/headerfiles.md)**
- **[namespaces](../docs/namespaces.md)**
- **[array](../docs/array.md)**
- **[Home](../README.md)**
