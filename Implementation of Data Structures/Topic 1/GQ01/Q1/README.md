
#Consider the following program

```cpp
#include <iostream>
using namespace std;

class Human{
	protected:
		int age;
		int height;
		
	public:
		Human(int height, int age){
			this->height = height;
			this->age = age;
		}

		int getAge(){
			return age;		
		}

		int getHeight(){
			return height;
		}
};

class Boy: public Human{
	public:
		Boy(int height, int age): Human(height, age) {}
		int getHeight(){
			return height+5;
		}
};

class Girl: public Human{
	public:
		Girl(int height, int age): Human(height, age) {}
		int getAge(){
			return age-2;
		}
};

int main(){

	Boy b(114,37);
	Girl g(114, 37);
	Human h(114, 37);
	
	cout << b.getAge() +
		  b.getHeight() +
		  g.getAge() +
		  g.getHeight() + 
		  h.getAge() +
		  h.getHeight();
	
	return 0;
}

```


What is the output of above program?

456
  correct 456
Explanation

This is a straight forward question on Inheritance.

The methods in the child class override the methods in the parent class.
