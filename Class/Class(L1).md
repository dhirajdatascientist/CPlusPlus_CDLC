```C++
#include <iostream>
#include <string>

using namespace std;

class Dog {
private:
    string name;

public:
    void setName(string n) {
        name = n;
    }

    string getName() {
        return name;
    }

    void bark() {
        cout << name << " says: Woof!" << endl;
    }
};

int main() {
    Dog myDog;          // Create a Dog object
    myDog.setName("Buddy");   // Set its name to "Buddy"
    cout << "The dog's name is: " << myDog.getName() << endl;
    myDog.bark();       // Buddy says: Woof!
    
    return 0;
}
```

## Example_002

```cpp
#include <iostream>
#include <string>

using namespace std;

class Employee {
private:
    string name;
    int id;
    double salary;

public:
    void setName(string n) {
        name = n;
    }

    string getName() {
        return name;
    }

    void setID(int i) {
        id = i;
    }

    int getID() {
        return id;
    }

    void setSalary(double s) {
        salary = s;
    }

    double getSalary() {
        return salary;
    }

    void displayInfo() {
        cout << "Employee Name: " << name << endl;
        cout << "Employee ID: " << id << endl;
        cout << "Employee Salary: $" << salary << endl;
    }
};

int main() {
    Employee emp1;        
    emp1.setName("John Doe");
    emp1.setID(1001);
    emp1.setSalary(50000.0);
    emp1.displayInfo();

    return 0;
}
```

**Question:**
You have been provided with a basic program that uses a class named `Employee`. The class has three private members: name (of type string), id (of type int), and salary (of type double). There are corresponding getter and setter functions for each of these members. Additionally, there's a member function named `displayInfo()` that displays the employee details.

Based on the provided code:

1. Modify the program to add another employee object, set its details, and display its information.
2. Add another member variable `position` to the class to store the job position of the employee (e.g., "Manager", "Developer", etc.). Also, add the corresponding getter and setter functions for this new member.
3. Enhance the `displayInfo()` function to also display the position of the employee.

Provide the modified code.
```