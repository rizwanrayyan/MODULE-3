# Ex.No:3
# Ex.Name: Write a C++ program to find the circumference of a circle using simple inheritance.
(Give private access of a base class to derived class. calculate the cube value using a member function of a base class and display the result using a member function of a derived class)
## Date: 21/08/2025
## Aim:
To write a C++ program to find the circumference of a circle using simple inheritance, where the radius is taken as a private member in the base class, cube value is calculated using a base class function, and the circumference is displayed using a derived class function.

## Algorithm:
```
1. Start the program.
2. Create a base class Circle with:
  -A private data member radius.
  -A public function to input the radius.
  -A public function getCube() to return the cube of the radius.
3. Create a derived class Circumference from Circle.
4. Define a member function to calculate and display the circumference of the circle using the formula:
5. Circumference=2×𝜋×radius
6. Also display the cube of the radius by calling the base class function.
7. In main(), create an object of Circumference, read the radius, and display the results.
8. End the program.
```



## Program:
```cpp
#include <iostream>
using namespace std;

class Circle {
private:
    float radius;

public:
    void read() {
        cin >> radius;
    }

    float getCircumference() {
        return 2 * 3.14 * radius;
    }
};

class Result : public Circle {
public:
    void display() {
        read();
        float c = getCircumference();
        cout << "Circumference of a circle is : " << c << endl;
    }
};

int main() {
    Result r1;
    r1.display();  
    return 0;
}
```


## Output:
<img width="612" height="211" alt="image" src="https://github.com/user-attachments/assets/861bbe71-8836-480d-bb17-fb1a3ebbeaae" />



## Result:
The program successfully demonstrates simple inheritance in C++ by calculating the circumference of a circle using the base class (with private data access) and also displaying the cube of the radius through a base class function.
