---
description: "Learn how to handle with streams"
title: "Stream Handling"
ms.date: 19/11/2023
ms.topic: "conceptual"
author: fejo-git
ms.reviewer: ---
---

## Streams

### escaping sign

"\" is a escaping sign.

```cpp

std::cout << "House\"A"

// output: House"A

```

In the code example: The escaping character ensures that the output doesn't prematurely terminate at "Haus," preventing a syntax error. Instead, it informs the compiler to include the quotation marks around "Haus" in the output.

### output in a .txt file

Output to the path `C:/user/` with the name "output" as a text file (`.txt`).

```cpp

ofstream file("C:/user/output.txt");

```

### write in a file

In this code, a string "Hello World" is written to the file. The file must be opened `file.open()` before writing to it and should be closed `file.close()` after use.

```cpp

file << "Hello World!" << endl;

```

### input from a file

Input for the path: `C:/user/`, with the name "output," and the file type as "txt."

```cpp

ifstream  file("C:/user/output.txt");

```

### read from file

In this code, data is read from the file and stored in the variable 'a'. The file must be opened `file.open()` before reading, and it should be closed `file.close()` after use.

```cpp

file >> a;

```

### check-if-file-exists

Here, we have an IF statement to check if the file was successfully opened. If it was opened, we then proceed to read the file until the end (file.eof = file end of line). This is where you should place the code for what you want to do with the read file, such as counting words. After that, the file is closed.

If the file was not successfully opened, the code will go into the else branch and output an error message "File could not be opened!"

```cpp

if(file.is_open()) {
    while(!file.eof()) {
            // Read until the end of the file
            // The code for what to do with the file should be here
            file.close();
    }
}

else {
    std::cout << "Datei konnte nicht geöffnet werden!" << endl;
}

```

### read lines

This command reads a line from the file and stores it in the String variable 'name'. 'name' should be declared before using this command.

```cpp

getline(cin, name);

```

### See also

- **[stringstream](../docs/stringstream.md)**
- **[string](../docs/string.md)**
- **[c-string](../docs/c-string.md)**
- **[Home](../README.md)**
