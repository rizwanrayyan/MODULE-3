# Ex.No:2
# Ex.Name: write a program to check whether student is passed the exam and display their grades using Multilevel inheritance?
(check if average > 90  grade=s,average >80 and less than equal to 90 A+ grade,average>70 and less than equal to 80 A grade,average 60 to 70 b grade,average is 50 to 59 C grade otherwise fail)
## Date: 21/08/2025
## Aim:
To write a C++ program using multilevel inheritance to check whether a student has passed the exam and display their grade based on the average marks.

## Algorithm:
1. Start the program.
2. Create a base class Student with data members for marks in subjects.
3. Derive a class Result from Student to calculate the average.
4. Derive another class Grade from Result to determine the grade based on the average using the conditions:
    -Average > 90 → Grade S
    -80 < Average ≤ 90 → Grade A+
    -70 < Average ≤ 80 → Grade A
    -60 ≤ Average ≤ 70 → Grade B
    -50 ≤ Average ≤ 59 → Grade C
    -Otherwise → Fail
5. In main(), create an object of Grade, input marks, calculate average, and display grade.
6. End the program.


## Program:
```cpp
#include <iostream>
using namespace std;

class A
{
    public:
    
        int sno,mark[5],tot=0,avg;
        string name,grade;
        
        void read(){
            cin>>sno>>name;
            for(int i=0;i<5;i++){
                cin>>mark[i];
                tot += mark[i];
            }
        }
};

class B:public A
{
    public:
        void calc(){
            //tot = s1+s2+s3+s4+s5;
            avg = tot/5;
            if(avg>90){
                grade = "S";
            }
            else if(avg>80 && avg<=90){
                grade = "A+";
            }
            else if(avg>70 && avg<=80){
                grade = "A";
            }
            else if(avg>60 && avg<=70){
                grade = "B";
            }
            else if(avg>50 && avg<=59){
                grade = "C";
            }
            else{
                grade = "F";
            }
        }
};

class C:public B
{
    public:
    
        void display(){
            cout<<"Student Number:"<<sno<<endl;
            cout<<"Student Name:"<<name<<endl;
            cout<<"Total:"<<tot<<endl;
            cout<<"Average:"<<avg<<endl;
            cout<<"Grade:"<<grade<<endl;
        }
};

int main()
{
    C obj;
    obj.read();
    obj.calc();
    obj.display();
}
```


## Output:
<img width="655" height="408" alt="image" src="https://github.com/user-attachments/assets/6c0d7017-e622-45a0-b37f-051b9d7cc8db" />



## Result:
The program successfully uses multilevel inheritance to check if a student has passed and displays their grade according to their average marks.

