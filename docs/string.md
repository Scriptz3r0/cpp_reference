---
description: "Learn how to handle with strings"
title: "String Handling"
ms.date: 19/11/2023
ms.topic: "conceptual"
author: fejo-git
ms.reviewer: ---
---

## String Handling

### get length of a string

The length( ) or size( ) function returns the length of the string.

```cpp
std::string s = "Hallo Welt";
std::cout << s.length();

// output: 10

```

```cpp
std::string s = "Hallo Welt";
std::cout << s.size();

// output: 10

```

In the code example: The length of the string with 10 characters is returned.

### get access of an individual character within a string

Using the s[2] notation, you can access each character in the string. Be cautious, as you can also access characters outside the string, for example, s[25]. This memory location is not declared and thus undefined.

```cpp
std::string s = "Hallo Welt";
std::cout << s[2];

// output: l

```

In the code example: We access position 2 in the string and print the character at that position.

### get access of an part from a string

Using string.substr(x, y), you can create and access a substring. You specify 'x' as the position for the substring, and 'y' as the number of characters you want in the substring.

```cpp
std::string s = "Hallo Welt";
std::cout << s.substr(0,4);

// output: Hall

```

In the code example: We create a substring starting at position '0' with a length of 4 characters.

### search for a character within a string

You can search for a character in a string. If the letter is present in the string, its position is returned as the result. If the letter appears multiple times in the string, the position of the first occurrence is returned. If the character is not found in the string, the string::npos value is returned (18446744073709551615).

```cpp
std::string s = "Hallo Welt";
std::cout << s.find("X");

// output: 18446744073709551615

```

In the code example: "X" could not be found in the string, and that's why the string::npos value is returned.

### return value to indicate that a character was not found in a string

string::npos is the return value when the character is not found in the string (string.find("X")).
You can further process this return value using if statements, for example.

```cpp
std::cout << std::string::npos;

// output: 18446744073709551615

```

### access values within a string and handle situations

If the value is outside the declared string's bounds, the program will terminate. Accessing s[13] would return an undefined value.

```cpp
std::string s = "Hallo Welt";
std::cout << s.at(2);

// output: l

```

### swap a single character within a string

Replace a character with another at any position.

```cpp
std::string s = "Hallo Welt";
s[0] = 'X';
std::cout << s;

// output: Xallo Welt

```

In the code example: Replace the 'H' with 'X' at position '0'.

### append a single character on a string

Append any number of characters at the end.

```cpp
std::string s = "Hallo Welt";
std::cout << s.append("!!!");

// output: Hallo Welt!!!

```

In the code example: Append '!!!' at the end.

### append a sindgle character within a string

Insert any number of characters at any position.

```cpp
std::string s = "Hallo Welt";
std::cout << s.insert(5,",");

// output: Hallo, Welt

```

In the code example: Insert a ',' (comma) at position 5.

### delete a single character within a string

Delete any number of characters at any position in the string.

```cpp
std::string s = "Hallo Welt";
std::cout << s.erase(4,1);

// output: Hall Welt
```

In the code example: Delete 1 character at position 4.

### See also

- **[c-string](../docs/c-string.md)**
- **[stringstream](../docs/stringstream.md)**
- **[standard-library](../docs/standard_library_overview.md)**
- **[Home](../README.md)**
