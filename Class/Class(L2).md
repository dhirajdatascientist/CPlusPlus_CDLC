### 1. Modify the program to add another employee object:

To do this, we will simply create another `Employee` object, set its details, and then display its information.

### 2. Add another member variable `position`:

We'll add a new private member `position` of type `string` to the `Employee` class. We'll also add corresponding getter and setter methods for it.

### 3. Enhance the `displayInfo()` function:

We'll modify the `displayInfo()` function to display the `position` of the employee.

Here's the modified code:

```cpp
#include <iostream>
#include <string>

using namespace std;

class Employee {
private:
    string name;
    int id;
    double salary;
    string position; // Added member variable for position

public:
    // Setters
    void setName(string n) {
        name = n;
    }

    void setID(int i) {
        id = i;
    }

    void setSalary(double s) {
        salary = s;
    }

    void setPosition(string p) { // Setter for position
        position = p;
    }

    // Getters
    string getName() {
        return name;
    }

    int getID() {
        return id;
    }

    double getSalary() {
        return salary;
    }

    string getPosition() { // Getter for position
        return position;
    }

    // Display function
    void displayInfo() {
        cout << "Employee Name: " << name << endl;
        cout << "Employee ID: " << id << endl;
        cout << "Employee Position: " << position << endl; // Displaying position
        cout << "Employee Salary: $" << salary << endl;
    }
};

int main() {
    Employee emp1;
    emp1.setName("John Doe");
    emp1.setID(1001);
    emp1.setSalary(50000.0);
    emp1.setPosition("Developer"); // Setting position for emp1
    emp1.displayInfo();

    cout << "--------------------" << endl; // Just for separation

    Employee emp2; // Another employee object
    emp2.setName("Jane Smith");
    emp2.setID(1002);
    emp2.setSalary(60000.0);
    emp2.setPosition("Manager"); // Setting position for emp2
    emp2.displayInfo();

    return 0;
}
```
