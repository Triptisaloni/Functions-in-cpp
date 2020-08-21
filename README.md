# Functions-in-cpp
10.Functions

A function is a group of statements that perform a particular task.
You may define your own functions in C++.

Using functions can have many advantages, including the following:
- You can reuse the code within a function.
- You can easily test individual functions.
- If it's necessary to make any code modifications, you can make modifications within a single function, without altering the program structure.
- You can use the same function for different inputs.
Every valid C++ program has at least one function - the main() function.

void is basic data type defines valueless---- no need of getch() in void functions

Syntax of defining a function: 
return_type function_name( parameter list )
{
body of the function
}


You must declare a function before calling it

#include <iostream>
using namespace std;

void printSomething() {
cout << "Hi there!";
}

int main() {
printSomething();

return 0;
}

Functions Parameters
#include <iostream>
using namespace std;

int printSomething(int x) {
return x;
}

int main() {
printSomething(42);
}

// Outputs 42


Multiple Parameters

int addNumbers(int x, int y) 
{
int result = x + y;
return result;
}
int main() {
cout << addNumbers(50, 25);
// Outputs 75
}

Datatype and name should be defined for each parameter

 rand()
to generate random numbers
<cstlib> header file is used

Srand()
The srand() function is used to generate truly random numbers.

Function Overloading

--To create multiple functions of same name

void printNumber(int a) {                 void printNumber (float a) {
cout<< a;                                 cout << a;
}                                        }

--By changing the return type we cant overload the functions

int printName(int a) { }       ||
float printName(int b) { }     || ---------the only difference from one to the other is 
double printName(int c) { }    ||         the return type, which is not allowed.
