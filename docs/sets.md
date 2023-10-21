---
description: "Learn how to Handle with Sets"
title: "Sets Handling"
ms.date: 05/11/2023
ms.topic: "conceptual"
author: fejo-git
ms.reviewer: ---
---

## Sets

### definition

- Each entry can only occur once.
- Similar to a list or vector.
- Sorts the variables within the set.

### code-example

```cpp
#include <set>
#include <iostream>

int main() {
    std::set<std::string> words = {"Hallo", "Welt"};
    words.insert("Mars");

    for(const auto &word : words) {
        std::cout << word << std::endl;
    }
}

// Ausgabe:
// Hallo
// Mars
// Welt

```

How many words are stored in the set.

```cpp
words.size();

```

How many times does 'Mars' appear in the set. It can only be 0 or 1, as each entry can only occur once.

```cpp
words.count("Mars");

```

### code-example2

```cpp
#include <iostream>
#include <set>
#include <fstream>

using namespace std;

int main() {

ifstream file("/users/test.txt");
if(file.is_open()) {
        cout << "The file could not be opened." << endl;
}
else {
        string word;
        set<string> words;
        while(!file.eof()) {
                file >>word;
                words.insert(word);
        }
        cout << words.size() << "different words were read in." << endl;
        file.close();
}
return 0;
}

```

### See also

- **[streams](../docs/streams.md)**
- **[standard library](../docs/standard_library_overview.md)**
- **[string](../docs/string.md)**
- **[Home](../README.md)**
