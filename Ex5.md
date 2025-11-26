# Ex.No:5
# Ex.Name: Write a C++ program to illustrate Discount Based Multiple inheritance with protected access specifier, find the amount payable after discount.
( Declare a base class to get original bill amount, another base class to get discount amount , declare a offer derived class to call the functions from two base classes and perform calculation)
## Date: 21/08/2025
## Aim:
To write a C++ program to illustrate discount calculation using multiple inheritance with protected access specifier, and find the amount payable after applying the discount.

## Algorithm:
```
1. Start the program.
2. Define a base class Bill with:
  A protected member billAmount.
  A public function to input the original bill amount.
3. Define another base class Discount with:
  A protected member discountPercent.
  A public function to input the discount percentage.
4. Define a derived class Offer which inherits both Bill and Discount using protected inheritance.
  Add a member function to calculate the discount and final payable amount.
  Display the original bill, discount, and net amount payable.
5. In main(), create an object of Offer, input details, and call the calculation function.
6. End the program.
```
## Program:
```cpp
#include <iostream>
using namespace std;
class OriginalAmount {
protected:
    float billAmount;

public:
    void getBillAmount() {
        cin >> billAmount;
    }
};

class Discount {
protected:
    float discountAmount;

public:
    void getDiscount() {
        
        cin >> discountAmount;
    }
};

class Offer : public OriginalAmount, public Discount {
public:
    void calculatePayable() {
        float payable = billAmount - discountAmount;
        cout << "Income after the payment of Tax : " << payable << endl;
    }
};

int main() {
    Offer obj;
    obj.getBillAmount();
    obj.getDiscount();
    obj.calculatePayable();
    return 0;
}
```


## Output:
<img width="725" height="275" alt="image" src="https://github.com/user-attachments/assets/8c6921bf-eb3a-455a-8ee7-c18ecef09f97" />



## Result:
The program successfully demonstrates multiple inheritance with protected access specifier to calculate the net amount payable after applying a discount on the original bill.
