# Ex.No:1
# Ex.Name: Write a C++ program to divide numbers using inheritance (declare two input variable as protected in base class and read one value in one derived class and read another value its derived class and do the divide operation in its derived class).
## Date: 21/08/2025
## Aim:
To write a C++ program to divide two numbers using inheritance, where two input variables are declared as protected in the base class, one value is read in the first derived class, the other value is read in the second derived class, and the divide operation is performed in the second derived cla

## Algorithm:
1. Start the program.
2. Define a base class Base with two protected data members a and b.
3. Define a derived class First from Base to read the first number into a.
4. Define another derived class Second from First to read the second number into b and perform division (a / b).
5. In main(), create an object of the class Second.
6. Call functions in sequence:
7. First derived class function to input the first number.
8. Second derived class function to input the second number.
9. Division function in the second derived class to compute and display the result.
10. End the program.




## Program:
```cpp
#include <iostream>
using namespace std;
class Base {
      protected:
      int a,b;
};

class A:public Base
{
    public:
        void read1(){
            cin>>a;
        }
};

class B:public A
{
    public:
    
        void read2(){
            cin>>b;
        }
};

class C:public B
{
    public:
    
        void display(){
            cout<<"The Result is:"<<a/b<<endl;
        }
};

int main()
{
    C obj;
    obj.read1();
    obj.read2();
    obj.display();
}
```


## Output:
<img width="471" height="227" alt="image" src="https://github.com/user-attachments/assets/a7a1ca9e-3bf6-46c6-acde-0825c2d584ff" />



## Result:
The program successfully demonstrates inheritance in C++ by reading the first value in one derived class, the second value in another derived class, and performing division in the second derived class.
