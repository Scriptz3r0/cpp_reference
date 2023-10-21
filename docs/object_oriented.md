---
description: "Learn how to handle Object Oriented"
title: "Object Oriented"
ms.date: 05/11/2023
ms.topic: "conceptual"
author: fejo-git
ms.reviewer: ---
---

## Object Oriented

### syntax class

object type / class: car
instance: the car, that is in my garage.
property: color green, 4 doors, shock absorber defective
methods: drive, smoke, noise

```cpp
class Car {

public:
 std::string brand;
 int ps;

void printcar() {
 std::cout << brand << " : " << ps;
}
};

int main() {

Car C;
C.brand = "bmw";
C.ps = 330;

Car C2;
C2.brand = "mercedes";
C2.ps = 330;

C.printcar();
C2.printcar();
}

```

### constructor

Is always executed whenever a new instance is created.

```cpp
class Car {
public:
 std::string brand;
 int ps;

Car(std::string brandP, int psP) {
 brand = brandP;
 ps = psP;
 std::cout << "Ein neues Auto wird erstellt" << std::endl;
}
void printCar() {
 std::cout << brand << " : " << ps << std::endl;
}
};

int main() {
Car c ("bmw", 330);
Car c2("mercedes", 330);

c.printcar();
c2.printcar();
}

```

The constructor enforces the input of a brand and horsepower.

### encapsulation private methods

```cpp
class Car {
private:
 std::string brand;
 int ps;

public:
 Car(std::string brandP, int psP) {
        brand = brandP;
        ps = psP;
        std::cout << "A new car is being created." << std::endl;
 }
 void tune() {
        ps += 20;
 }
 void printCar() {
        std::cout << brand << " : " << ps << std::endl;
 }
};

int main() {

Car c("bmw" , 330);
Car c2("mercedes", 330);

c2.tune();

c.printCar();
c2.printCar();
}

// output:
//A new car is being created.
//A new car is being created.
//bmw : 330
//mercedes : 350

```

Variables and methods marked as 'private' can only be modified or accessed within the Car class.

### keyword this

```cpp
class Car {
private:
 std::string brand;
 int ps;
public:
 Car(std::string brand, int ps) {
            this->brand = brand;
            this->ps = ps;
            std::cout << "Ein neues Auto wird erstellt" << std::endl;
 }
};

```

"The 'this' keyword accesses the variable in 'private' and not the passed parameter. Within a class, 'this' is used to access class properties, while from outside, it's accessed with 'c.printCar()'."

### getter and setter

GET-method or GETTER

```cpp
std::string getBrand() {
    return brand;
}

int getPs() {
    return ps;
}

```

SET-methods or SETTER

```cpp
void setPs(int ps) {
    if(ps > 1000) {
            std::cout << "Thats not possible!" << std::endl;
    }
    else {
            this->ps= ps;
    }
}

```

Both methods must be defined within the class.

```cpp
int main() {

c.setOs(307);
std::cout << c.getBrand() << std::endl;
std::cout << c.getPs() << std::endl;
}

```

Main program to call the two set and get methods.

### See also

- **[this vs c.property](../docs/this_vs_c.property.md)**
- **[encapsulation](../docs/encapsulation.md)**
- **[desctructor](../docs/destructor.md)**
- **[overload cunstructors](../docs/overload_cunstructor.md)**
- **[Home](../README.md)**
