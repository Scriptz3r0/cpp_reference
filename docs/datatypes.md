---
description: "Learn how to Handle Datatypes"
title: "Datatype Handling"
ms.date: 05/11/2023
ms.topic: "conceptual"
author: fejo-git
ms.reviewer: ---
---

## Datatypes

### enum

With an ENUM, you have the 'status' type, which can take on various values. In this case, 'status' can be OFFLINE, ONLINE, AWAY, or BUSY. You can also access them with 0, 1, 2, 3, and 4, as these values are automatically assigned. However, you can also assign a value like 'OFFLINE = 1000' to set the value to 1000.

```cpp
enum status {
 OFFLINE,
 ONLINE,
 AWAY,
 BUSY
};

int main() {

status status = status::BUSY;

if(status == status::BUSY) {
 std::cout << "The User is busy!" << std::endl;
}

```

### pair

With a `pair`, you combine two data types together. In this case, you are combining a string with an integer.

```cpp
std::pair<std::string, int> p ("Hello World", 42);

std::cout << p.first << std::endl;
std::cout << p.second << std::endl;

// output:
// Hello World
// 42

```

By using `p.second = 13`, you are assigning the value 13 to the integer variable within the pair.

```cpp
p.second = 13;

```

### maps

Using `map` in C++, you can store a mapping where there are key-value pairs. A map allows you to store and retrieve values based on keys, similar to a phone book, where the family name "Mustermann" is the key, and the phone number is the associated value.

A map provides an efficient way to search for a key and retrieve the associated value, making it particularly useful for many applications where you want to associate data with keys.

Create a map with a `std::pair` of a string key and an integer value.

```cpp
#include <map>

std::map<std::string, int> m;
m.insert(std::pair<std::string, int> ("Müller", 321);

```

Returns the count of all entries in the map.

```cpp
m.size();

```

Output of 321. Using `at()`, it checks if the entry exists.

```cpp
m.at("Mueller");

```

Output of 321. It does not check if the entry exists.

```cpp
m[Mueller];

```

Assign a new value to the entry "Mueller."

```cpp
m[Mueller] = 555;

```

```cpp
#include <iostream>
#include <string>
#include <vector>
#include <utility>
#include <map>

using namespace std;

int main() {

vector<string> words = {"Hello", "World", "Welt", "Mars"};

map<string, int> occurences;

for(const string &word : words) {
    if(occurences.count(word) == 0) {
            occurences.insert(pair<string, int> (word, 1));
    }
    else {
            occurences[word]++;
    }
}


// An alternative but slower method.

int welt = 0;
for(const string &word : words) {
    if(word == "World") {
            welt++;
    }
 }

cout << welt << endl;

cout << occurences.at("World") << endl;
cout << occurences.at("Mars") << endl;

return 0;

}

```

### encapsulation with map

```cpp
#include <iostream>
#include <string>
#include <vector>
#include <utility>
#include <map>

using namespace std;

class PhoneBook {
private:
 map<string, int> phoneBook;

public:
 void addEntry(string name, int phoneNumber) {
        phoneBook.insert(pair<string, int> (name, phoneNumber));
 }
};

void doSomething(const PhoneBook &phoneBook) {
// Code
}

int main() {
PhoneBook phoneBook;
doSomething(phoneBook);
return 0;
}

```

### priority queue

- Priority queue
- Automatically sorted
- Can only access the first element at all times

```cpp
priority_queue <pair<int, string>> pq;
pq.push(pair<int,string> (123, "Hello"));
cout << pq.top().first << pq.top().second;
pq.pop();

```

### See also

- **[standard library](../docs/standard_library_overview.md)**
- **[statements](../docs/statements.md)**
- **[vector](../docs/vector.md)**
- **[Home](../README.md)**
