---
description: "Learn how to Handle with Operators (C++ or ++C)"
title: "Operator Handling"
ms.date: 19/11/2023
ms.topic: "conceptual"
author: fejo-git
ms.reviewer: ---
---

## Operators

### definition

In C++, when using `++` as a prefix (`++C`), the variable is first incremented, and then its value is used.

On the other hand, in C++, when using `++` as a postfix (`C++`), the current value of the variable is used, and then it is incremented.

The direction in which the operation is performed (left-to-right or right-to-left) depends on the context in which it is used in an expression.

### overload operator

```cpp
#include <iostream>
#include <string>

using namespace std;

class Auto {
private:
    int ps_;

public:
    Auto(int ps) {
            ps_ = ps;
    }

    bool hasMorePs(const Auto &other) {
            return (this->ps_ > other.ps_);
    }

    int getPs() {
            return ps_;
    }

    Auto& operator ++() {
            ps_++;
            return *this;
    }

    Auto operator ++(int) {
            Auto tmp(*this);
            ps_++;
            return tmp;
    }

    bool operator <(const Auto &other) const {
            return (ps_ < other.ps_);
    }

    bool operator > (const Auto &other) const {
            return (ps_ > other.ps);
    }
};

```

main programm

```cpp
int main() {

Auto a(250);
Auto b(330);

int c = 5;
cout << c++ << endl;
cout << c << endl;

++a;
a++;

cout << (a++).getPs() << endl;
cout << a.getPs() << endl;

cout << (a < b) << endl;
cout << (b > a) << endl;

cout << a.hasMorePs(b) << endl;
cout << b.hasMorePs(a) << endl;
return 0;
}

```

### See also

- **[exceptions](../docs/exceptions.md)**
- **[statements](../docs/statements.md)**
- **[algorithm](../docs/algorithm.md)**
- **[Home](../README.md)**
