---
description: "Learn how to Handle with Exceptions"
title: "Exceptions Handling"
ms.date: 19/11/2023
ms.topic: "conceptual"
author: fejo-git
ms.reviewer: ---
---

## Exceptions

### definition

- Catch errors to allow the program to continue running.
- Works across multiple levels.
- Custom exceptions can be programmed.

```cpp
#include <iostream>
#include <vector>
#include <stdexception>

using namespace std;

void doSomething() {
    vector<string> data = {"Maria"};
    cout << data.at(2) << endl;
}

int main() {
try {doSomething();}
catch (out_of_range &e) {
    cout << "Es ist ein out_of_range_Fehler aufgetreten" << endl;
}

```

The try block is terminated in case of an error.

### exception thrown manually

```cpp
class InvalidParameter {};

void doSomething(int n) {
    if(n == 0) {
            throw InvalidParameter();
    }
    cout << (10/n) << endl;
}

int main() {
try { doSomething(0);}
catch(out_of_range &e) {
        cout << "out_of_range_Fehler" << endl;
}
catch(InvalidParameter &e) {
        cout << "InvalidParameter_Fehler" << endl;
}

```

### expand std::exception

```cpp
#include <iostream>
#include <stdexcept>

using namespace std;

class InvalidParameter : public exceptopm {
        virtual const char* what();
        const noexcept {
                return "Invalid Parameter";}
};

void doSomething(int n) {
        if(n == 0) {
                throw InvalidParameter();
        }
        cout << (10/n) << endl;
}

int main() {
try {
        doSomething(0);
}
catch(exception &e) {
        const cahr* w = e.what();
        cout << "Es ist eine Fehler aufgetreten: " << w << endl;
}
}

```

### See also

- **[headerfiles](../docs/headerfiles.md)**
- **[functions](../docs/functions.md)**
- **[standard library overview](../docs/standard_library_overview.md)**
- **[Home](../README.md)**
