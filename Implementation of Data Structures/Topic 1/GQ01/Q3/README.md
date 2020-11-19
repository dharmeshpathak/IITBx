Consider the following C++ program with unspecified expressions Expr1 and Expr2

```cpp

#include <iostream>
#include <cstdlib>
using namespace std;

struct A{
  int x;
  int y;
  int z;
};

struct A* D(int x, int y, int z){
  Expr1 
  (*C).x=x*y;
  (*C).y=y*z;
  (*C).z=x*z;
  return C;
}

int main(){
  int a=2, b=3, c=4;
  Expr2 
  E = D(a, b, c);
}

```  

Expressions Expr1 and Expr2 need to be identified, such that the value of '(*E).x', '(*E).y', and '(*E).z' are 6, 12, and 8 respectively.
Select an appropriate choice from the following:


Expr1 is required to be replaced by struct A* C = (struct A*) malloc(sizeof(struct A)); and Expr2 by struct A* E; correct


The correct answer is Expr1: struct A* C = (struct A*) malloc(sizeof(struct A)); and Expr2: struct A* E;

In 'Expr2', it is enough to just declare a pointer to a structure (struct A* E), rather than return a pointer to memory allocated of size 'struct A'.
In 'Expr1', it is required to dynamically allocate memory of size 'struct A' and return a pointer pointing to a structure 'A'.
The pointer address returned gets stored in C. It cannot be declared as just 'struct A *C' (in which case it will give "segmentation fault" because C is just a pointer.
Since no memory is allocated for C. C points to nothing but random garbage location. So accessing (*C).x results into segmentation fault.)
but need to be declared as 'struct A* C = (struct A*) malloc(sizeof(struct A));'

The remaining part of function 'D', a member element selection by reference i.e. '(*C).x', '(*C).y', and '(*C).z' is being used to initialize the new value of structure member variables 'x', 'y', and 'z' respectively. Using the variables passed to the function D(x=2, y=3, z=4), it effectively computes 6, 12, and 8 respectively. Thus, the value of '(*E).x', '(*E).y', and '(*E).z' are 6, 12, and 8 respectively.
