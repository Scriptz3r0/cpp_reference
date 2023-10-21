---
description: "Learn how to handle with Stringstreams"
title: "Stringstream Handling"
ms.date: 05/11/2023
ms.topic: "conceptual"
author: fejo-git
ms.reviewer: ---
---

## Stringstream

### Why using a stringstream

"Memory issue with String

Memory:

“Test123” 1234567

string.append(”Test”);

→ Nothing can be directly appended to the string in memory

→ The string needs to be copied to a new location

Memory:

1234567 “Test123Test”

It's slow because the old string must be copied, which is why a stringstream is used.

In a function, it's advisable to avoid using cout and instead use a string as the return value. In the main() function, the string can be printed or used in other ways."

### method stringstream

```cpp
#include <stringstream>
#include <iostream>

class Test {
private:
 vector<vector<int>> field;

public:
string getFieldStr() {
for(const auto &row : field) {
        result << " | ";
        for(const auto &item : row) {
                result << item << " | ";
        }
        result << endl;
}
resturn result.str();
}
};

```

### See also

- **[streams](../docs/streams.md)**
- **[string](../docs/string.md)**
- **[Home](../README.md)**
