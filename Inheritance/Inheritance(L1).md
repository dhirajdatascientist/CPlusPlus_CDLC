### Inheritance:

Inheritance is one of the four main principles of object-oriented programming (OOP). It allows you to define a new class based on an existing class. The new class inherits attributes and behavior (i.e., fields and methods) from the existing class.

**Why Use Inheritance?**

1. **Reuse of Code**: One of the main benefits of inheritance is code reusability. Once a behavior (method) is defined in a superclass, that behavior can be inherited and used by all derived classes, without the need to rewrite the same code.

2. **Extensibility**: It provides a mechanism to add additional features to an existing class without modifying it, by simply extending it.

3. **Provides Hierarchical Classification**: It provides a clear model structure which is easy to understand without much complexity.

4. **Form of Polymorphism**: It provides an ability to use a class exactly like its parent so there's no need to redefine methods available in the parent class, but you can also override methods if needed.

### Simple Example:

Consider a general class `Vehicle` and a specific class `Car` that inherits from `Vehicle`.

```cpp
#include <iostream>
using namespace std;

// Base class
class Vehicle {
public:
    void generalInfo() {
        cout << "This is a vehicle." << endl;
    }
};

// Derived class
class Car : public Vehicle {
public:
    void specificInfo() {
        cout << "This is a car." << endl;
    }
};

int main() {
    Car myCar;  // Creating an object of the derived class
    myCar.generalInfo();  // Method from the base class
    myCar.specificInfo();  // Method from the derived class
    return 0;
}
```

In this example:
- `Vehicle` is the **base class** (or parent class).
- `Car` is the **derived class** (or child class) that inherits from `Vehicle`.
- We defined a method `generalInfo()` in the base class and another method `specificInfo()` in the derived class.
- The object `myCar` of the derived class `Car` can access both the methods from the base class and the derived class, demonstrating the concept of inheritance.

This is a simple example, but inheritance can be much more complex and versatile in real-world applications. It can help in modeling and designing more complex relationships between entities.