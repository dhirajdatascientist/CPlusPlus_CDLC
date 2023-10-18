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