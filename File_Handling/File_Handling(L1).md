* File handling is an essential aspect of most programming languages, allowing data to be saved and retrieved from files. 
* In C++, the file handling mechanisms are provided by the `fstream` library.

## File handling in C++:

1. **Headers**:
    - `#include <fstream>`: This is required to work with file streams.

2. **Main Classes**:
    - `ofstream`: Output file stream (for writing to files).
    - `ifstream`: Input file stream (for reading from files).
    - `fstream`: Both input and output (for reading from and writing to files).

3. **Opening a File**:
    - Use the `open()` function.
    ```cpp
    ofstream outFile;
    outFile.open("example.txt");
    ```

4. **Closing a File**:
    - Use the `close()` function.
    ```cpp
    outFile.close();
    ```

5. **Writing to a File**:
    ```cpp
    outFile << "Hello, World!";
    ```

6. **Reading from a File**:
    ```cpp
    string line;
    ifstream inFile("example.txt");
    while (getline(inFile, line)) {
        cout << line << endl;
    }
    ```

7. **Checking for Errors**:
    - Use the `fail()` function to check if something went wrong.
    - Use the `eof()` function to check if the end of the file has been reached.

## Writes to and reads from a file:

```cpp
#include <iostream>
#include <fstream>
using namespace std;

// Function to write to a file
void writeToFile() {
    ofstream outFile("example.txt");
    if (!outFile) {
        cout << "Error writing to file!" << endl;
        return;
    }
    outFile << "Hello, World!" << endl;
    outFile.close();
}

// Function to read from a file
void readFromFile() {
    ifstream inFile("example.txt");
    if (!inFile) {
        cout << "Error reading from file!" << endl;
        return;
    }
    string line;
    while (getline(inFile, line)) {
        cout << line << endl;
    }
    inFile.close();
}

int main() {
    writeToFile();
    readFromFile();

    return 0;
}

```