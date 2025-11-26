# Ex.No:4
# Ex.Name: Write a CPP program to overload a function to print Integer data in one and Floating-Point data in another
## Date: 21/08/2025
## Aim:
To write a C++ program that overloads a function to print integer data in one version and floating-point data in another version.

## Algorithm:
1. Start the program.
2. Define a class Printer with two overloaded functions named print:
3. One function accepts an integer and prints it.
4. Another function accepts a floating-point value and prints it.
5. In main(), create an object of the class.
6. Call the print function with both integer and float values.
7. End the program.

## Program:
```cpp
#include<iostream>
using namespace std;
class display
{
    public:
    void print(int i)
    {
        cout<<"Integer="<<i<<endl;
    }
    void print(double f)
    {
        cout<<"Floating Point="<<f<<endl;
    }
};
int main()
{
    int a;
    double b;
    cin>>a>>b;
    display d;
    d.print(a);
    d.print(b);
}
```


## Output:
<img width="512" height="266" alt="image" src="https://github.com/user-attachments/assets/f51222b9-ebdf-40ac-aff1-c4224ef9d437" />



## Result:
The program successfully demonstrates function overloading in C++ by printing integer data in one function and floating-point data in another.
