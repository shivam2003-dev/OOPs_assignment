Welcome to the OOPs_assignment wiki!


   ## OOPs Assignment
   ---
  ###   Content
  ```
1. Use of Protected, Public , private Classes
2. Inline function
3. Using pointer to member, setw,new and delete operator
4. Usage of  .*  ::*   ->*
5. Cascading of operators
6. Friend functions
7. virtual function
8. Accessing inheritance of classes
9. Function overloading
10. Cascading using pointers
11. Passing function as an argument of function
12. Define struct inside class
13. Local and abstract classes
14. Properties and uses of constructor and destructor
15. constructor in Union
16. NumberSystem Conversion
17. Data Type Conversion
18. Perform operation on Strings(eg, check if a word is palindrome)
19. Operator overloading
20. Static members and functions
21. Ambiguity in inheritance
22. Constructors in inheritance
23. Sort elements of array using pointers
24. File I/O
25. Function Templates
26. Class Templates
27. Exception Handling
```

  
---
---
   ## Welcome to the OOPs_assignment !
                                      Name : Shivam Kumar 
                                Roll/Class : CO20350(cse)

### Program 1 : [Use of Protected, Public, private Classes](https://replit.com/@shivamkumar57/Programming#1_access_specifier.cpp)
---
```c++
#include <iostream>
using namespace std;

class Parent
{  
    private:
      int roll;
      string name;

    public:
      void Input()
      {  cout<<" Enter your tempId Number -> ";
        cin>>roll;
        cout<<" \nEnter your name -> ";
        cin>>name;
        cout<<"\n";
      }
      void displayDetail()
      { 
        cout<<":::  Roll ->  " <<roll<<"  :::  Name -> "<<name<<"\n";
      }
    protected:
    int id_protected;
    
};
class Child : public Parent
{
    public:
    void setId(int id)
    {   
        id_protected = id;  
    }
     
    void displayId()
    {
        cout << "Secret Id ->  " << id_protected <<"   ";
    }
};
int main() {
    Child obj1;
    Parent obj2;
    cout<<"\t\tWelcome To Secret Agency "<<"\n\n";
    cout<<"Get your Secret Id  \n";
    obj1.setId(rand());
    obj2.Input();
    obj1.displayId();
    obj2.displayDetail();
    return 0;
}
```



### PROGRAM 2: [Use of Inline Function](https://replit.com/@shivamkumar57/Programming#2_inline_fns.cpp)
---
```c++
//Use of Inline function

#include <iostream>

using namespace std;

  

class operation

{

int a,b,add,sub,mul;

float div;

public:

void Input();

void sum();

void difference();

void product();

void division();

};

inline void operation :: Input()

{

cout << "Enter first value:";

cin >> a;

cout << "Enter second value:";

cin >> b;

}

inline void operation :: sum()

{

add = a+b;

cout << "Addition of two numbers: " << a+b << "\n";

}

inline void operation :: difference()

{

sub = a-b;

cout << "Difference of two numbers: " << a-b << "\n";

}

inline void operation :: product()

{

mul = a*b;

cout << "Product of two numbers: " << a*b << "\n";

}

inline void operation ::division()

{

div=a/b;

cout<<"Division of two numbers: "<<a/b<<"\n" ;

}

int main()

{

cout << "Program using inline function\n";

operation n;

n.Input();

n.sum();

n.difference();

n.product();

n.division();

return 0;

}
```


### PROGRAM 3: [Using pointer to member, setw,new and delete operator](https://replit.com/@shivamkumar57/Programming#3_ptr_to_mbr.cpp)
---
```C++
// Using pointer to member, setw,new and delete operator

  

#include <iostream>

#include<iomanip>

using namespace std;

int main ()

{

int* p = NULL;

p = new int;

if (!p)

cout << "allocation of memory failed\n";

else

{

*p = 29;

cout << setw(5)<<"Value of p: " << *p << endl;

}

delete p;

return 0;

}
```


### PROGRAM 4 : [Usage of  .*  ::*   ->*  ](https://replit.com/@shivamkumar57/Programming#4_useofSomeOpt.cpp)
---
```C++ 
#include <iostream>

using namespace std;

  

class BinOpt {

public:

void m_func1() { cout << "m_func1\n"; }

int m_num;

};

  

void (BinOpt::*pmfn)() = &BinOpt::m_func1;

int BinOpt::*pmd = &BinOpt::m_num;

  

int main()

{

BinOpt obj;

BinOpt *obj2 = new BinOpt;

(obj.*pmfn)();

(obj2->*pmfn)();

obj.*pmd = 1;

obj2->*pmd = 2;

  

cout << obj.*pmd << endl

<< obj2->*pmd << endl;

  

delete obj2;

return 0;

}
```


### PROGRAM 5: [Cascading of operators](https://replit.com/@shivamkumar57/Programming#5_cascad_opt.cpp)
---
```C++
//Cascading of operators

#include<iostream>

using namespace std;

  

int main()

{

int a,b,sum;

cout<<"Enter value of a and b"<<"\n"; //cascading of <<

cin>>a>>b;

cout<<"\nsum = "<<a+b<<"\n";

return 0;

}
```


### PROGRAM 6 :[use of friends function](https://replit.com/@shivamkumar57/Programming#6_friendfns.cpp) 
---
```c++
//use of friends function

#include<iostream>

using namespace std;
class sample{
int a,b;
public:
void setvalue() { a=25; b=40; }
friend float mean(sample s);
};
float mean(sample s)
{
return float(s.a+s.b)/2.0;
}
int main()
{
sample x;
x.setvalue();
cout<<"Mean value = "<<mean(x)<<"\n";
return 0;

}
```


### PROGRAM 7 :[use of virtual function](https://replit.com/@shivamkumar57/Programming#7_virtual_fns.cpp)
---
```C++
/// use of virtual function

  

#include<iostream>

using namespace std;

  

class base{

public:

void display() { cout<< " \n Dispaly Base "; }

virtual void show()

{

cout<<"\n Show base ";

}

};

  

class derived : public base

{

public :

void display() { cout<<" \n Display derived " ; }

void show()

{

cout<<" \n show derived ";

}

};

  

int main()

{

base b;

derived d;

base *ptr;

  

cout<<" \n ptr points to base ";

ptr=&b;

ptr->display();

ptr->show();

  

cout<<" \n ptr points to derived ";

ptr=&d;

ptr->display();

ptr->show();

  

cout<<"\n";

  

return 0;

}
```


### PROGRAM 8: [Accessing inheritance of classes](https://replit.com/@shivamkumar57/Programming#8_access_inheritance_class.cpp)
---
```C++
#include <iostream>

using namespace std;

  

class Parent

{

public:

int id_p;

};

class Child : public Parent

{

public:

int id_c;

};

int main()

{

Child obj1;

obj1.id_c = 7;

obj1.id_p = 91;

cout << "Child id is " << obj1.id_c << endl;

cout << "Parent id is " << obj1.id_p << endl;

return 0;

}
```


### PROGRAM 9 : [FUNCTION OVERLOADING](https://replit.com/@shivamkumar57/Programming#9_funs_overload.cpp)
---
```c++
//Function overloading

#include<iostream>

using namespace std;

class A

{

public:

int area(int s ) { return s*s; }

int area(int l ,int b) { return 2*l*b; }

double area(double r) { return 3.14*r*r; }

  

};

  

int main()

{

A a;

int s,l,b,r;

cout<<" Area of Square : "<< a.area(4)<<endl;

cout<<" Area of rectangle : "<< a.area(5,4)<<endl;

cout<<"Area of circle : "<< a.area(7.00)<<endl;

  

return 0;

}
```


### PROGRAM 10 : [Cascading using pointers](https://replit.com/@shivamkumar57/Programming#10_cascading_using_ptr.cpp)
---
```c++
#include <iostream>

using namespace std;

class Square

{   

public:

int side;

Square area()

{

cout << "Area of the square is :" << side*side <<endl;

return *this;

}

Square perimeter()

{

cout << "Perimeter of the square is :" << 4*side <<endl;

return *this;

}

};

int main()

{

Square sq;

sq.side =3;

sq.area().perimeter();

return 0;

}
```


### PROGRAM 11 : [Passing function as an argument of function](https://replit.com/@shivamkumar57/Programming#11_fns_as_arg.cpp)
---
```c++
#include <bits/stdc++.h>

using namespace std;

  

int add(int x, int y){return x+y;}

int sub(int x, int y){return x-y;}

int operation (int x, int y,int (*function)(int,int)){return function(x,y);}

  

int operation2(int x, int y,std::function<int(int, int)> function){return function(x,y);}

  

int main()

{

  

//Method 1

std::cout <<"Values 1 & 3. Pointer function: Add:"<<operation (1,3,&add)<<" Sub:"<<operation (1,3,&sub) << std::endl;

  

//Method 2

std::cout <<"Values 1 & 3. std::function : Add:"<<operation2(1,3,&add)<<" Sub:"<<operation2(1,3,&sub) << std::endl;

}
```

### PROGRAM 12 : [STRUCT INSIDE THE CLASS](https://replit.com/@shivamkumar57/Programming#12_struct_inside_class.cpp)
---
```c++
#include <iostream>

using namespace std;

  

class E

{

public:

struct X { int v=10; };

X x; // an instance of `struct X`

};

  

int main(){

  

E object;

int ans =object.x.v ;

cout<<"ans: "<< ans<<endl;

return 0;

}
```
OUTPUT :
![[Screenshot (73).png]]

### PROGRAM 13 :[LOCAL AND ABSTACT CLASS](https://replit.com/@shivamkumar57/Programming#13_local_Abstract_class.cpp)
---
```c++
#include<iostream>

using namespace std;

//local class

void fun()

{

 class Test

 {

 public:

 void method() {

 cout << "Local Class method() called";

 }

};  

 Test t;

 t.method();

}


int main()

{

 fun();

 return 0;

}
```


### PROGRAM 14 : [CONSTRUCTOR AND DESTRUCTOR](https://replit.com/@shivamkumar57/Programming#14_constructor_des.cpp)
---
```c++
#include<iostream>

using namespace std;

  

class example{

public:

example() { //constructor

cout<<" Inside the constuctor \n";

}

~example() //destructor

{

cout<<" Inside the destructor \n";

}

  

};

  

int main()

{

example e;

return 0;

}
```



### PROGRAM 15 : [constructor in Union](https://replit.com/@shivamkumar57/Programming#15_constructor_in_union.cpp)
---
```c++
// C++ program to illustrate union

#include <bits/stdc++.h>

using namespace std;

  

union abc {

 int a;

int b;

int sum;

abc()

{

sum=0;

}

};
int main()

{
 union abc g;
g.a=5;

g.b=10;

int sum=g.a+g.b;

cout<<sum<<"\n";
 return 0;

}
```




### PROGRAM 16 ::[DECIMAL TO BINARY :NUM SYS CONVERSION](https://replit.com/@shivamkumar57/Programming#16_NumberSystemConversion.cpp)
---
```C++
#include<iostream>

#include<stack>

using namespace std;

void dec_to_bin(int number) {

stack<int> stk;

while(number > 0) {

int rem = number % 2; //take remainder

number = number / 2;

stk.push(rem);

}

while(!stk.empty()) {

int item;

item = stk.top();

stk.pop();

cout << item;

}

}

int main() {

int num;

cout << "Enter a number: ";

cin >> num;

dec_to_bin(num);

cout<<endl;

}
```
OUTPUT :
![[Screenshot (77).png]]

### PROGRAM 17 : [DATA TYPE CONVERSION](https://replit.com/@shivamkumar57/Programming#17_dataType_conversion.cpp)
---
```C++
#include <iostream>

using namespace std;

int main()

{

double x;

cout<<"Enter value of x in double :";

cin>> x;

  
  

int sum = (int)x + 1;

  

cout << "integer part of x++ = " << sum<<endl;

return 0;

}
```



### PROGRAM 18 : [PALLINDROME STRING](https://replit.com/@shivamkumar57/Programming#18_pallindrome_string.cpp)
---
```C++
#include <iostream>

#include<string.h>

  

using namespace std;

  

int main(){

char string1[20];

int i, length;

int flag = 0;

cout << "Enter a string: "; cin >> string1;

length = strlen(string1);

for(i=0;i < length ;i++){

if(string1[i] != string1[length-i-1]){

flag = 1;

break;

}

}

if (flag) {

cout << string1 << " is not a palindrome" << endl;

}

else {

cout << string1 << " is a palindrome" << endl;

}

return 0;

}
```



### PROGRAM 19 : [OPERATOR OVERLOADING](https://replit.com/@shivamkumar57/Programming#19_operator_overloading.cpp)
---
```C++
#include<iostream>

using namespace std;

  

class Complex {

private:

 int real, imag;

public:

 Complex(int r = 0, int i =0) {real = r; imag = i;}

 Complex operator + (Complex const &obj) {

 Complex res;

 res.real = real + obj.real;

 res.imag = imag + obj.imag;

 return res;

 }

 void print() { cout << real << " + i" << imag << endl; }

};

  

int main()

{

 Complex c1(10, 5), c2(2, 4);

 Complex c3 = c1 + c2;

 c3.print();

}
```


### PROGRAM 20 :[Static members and functions](https://replit.com/@shivamkumar57/Programming#20_static_member_fns.cpp)
---
```C++
#include <iostream>

using namespace std;

struct X {

private:

int i;

static int si;

public:

void set_i(int arg) { i = arg; }

static void set_si(int arg) { si = arg; }

  

void print_i() {

cout << "Value of i = " << i << endl;

cout << "Again, value of i = " << this->i << endl;

}

  

static void print_si() {

cout << "Value of si = " << si << endl;

}

  

};

  

int X::si = 77;

  

int main() {

X xobj;

xobj.set_i(11);

xobj.print_i();

X::print_si();

X::set_si(22);

X::print_si();

}
```


### PROGRAM 21 :[AMBIGUITY IN INHERITANCE](https://replit.com/@shivamkumar57/Programming#21_ambiguity_in_inheritance.cpp)
---
```C++
  

#include<iostream>

using namespace std;

class Parent_f

{

public:

void show()

{

cout<<"This is Parent_f\n";

}

};

class Parent_m

{

public:

void show()

{

cout<<"This is Parent_m\n";

}

};

class Son:public Parent_f,public Parent_m

{

public:

void display()

{

cout<<"This is son\n";

}

};

int main()

{

Son son;

son.show();

son.display();

cout << "Hello world!" << endl;

return 0;

}
```



### PROGRAM 22 :[CONSTRUCTOR IN INHERITANCE](https://replit.com/@shivamkumar57/Programming#22_constructor_in_inheritance.cpp)
---
```C++
#include<iostream>

using namespace std;

class parent

{

public:

parent()

{

cout<<"Parent class Constructor\n";

}

~parent()

{

cout<<"Parent class Destructor\n";

}

};

  

class child : public parent

{

public:

child()

{

cout<<"Child class Constructor\n";

}

~ child()

{

cout<<"Child class Destructor\n";

}

};

  

int main()

{

child c;

return 0;

}
```





### PROGRAM 23 :[SORT ARRAY USING POINTER](https://replit.com/@shivamkumar57/Programming#23_sort_array_using_ptr.cpp)
---

```C++
#include <iostream>

using namespace std;

void sort(int n, int *ptr)

{

 int i, j, t;

 for (i = 0; i < n; i++)

 {

 for (j = i + 1; j < n; j++)

 {

 if (*(ptr + j) < *(ptr + i))

 {

 t = *(ptr + i);

 *(ptr + i) = *(ptr + j);

 *(ptr + j) = t;

 }

 }

 }

 for (i = 0; i < n; i++)

 cout << *(ptr + i) << " ";

cout<<endl;

}

int main()

{

 int n = 5;

 int arr[] = {0, 23, 14, 12, 9};

 sort(n, arr);

 return 0;

}
```




### PROGRAM 24: [FILE HANDLING](https://replit.com/@shivamkumar57/Programming#24_file_io.cpp)
---

```C++
  

#include <iostream>

#include <fstream>

using namespace std;

int main()

{

 ofstream fout;

 string line;

 fout.open("sample.txt");

 while (fout)

 {

 getline(cin, line);

 if (line == "-1")

 break;

 fout << line << endl;

 }

 fout.close();

 ifstream fin;

 fin.open("sample.txt");

 while (fin)

 {

 getline(fin, line);

 cout << line << endl;

 }

 fin.close();

 return 0;

}
```


### PROGRAM 25: [FUNCTION TEMPLATE ](https://replit.com/@shivamkumar57/Programming#25_function_template.cpp)
---
```C++
#include <iostream>

using namespace std;

  

template <typename T>

T add(T num1, T num2) {

return (num1 + num2);

}

  

int main() {

int result1;

double result2;

result1 = add<int>(2, 3);

cout << "2 + 3 = " << result1 << endl;

  

result2 = add<double>(2.2, 3.3);

cout << "2.2 + 3.3 = " << result2 << endl;

  

return 0;

}
```


### PROGRAM 26 : [CLASS TEMPLATE](https://replit.com/@shivamkumar57/Programming#26_class_tempelate.cpp)

---
```C++
#include <iostream>

#include <cstdlib>

using namespace std;

  

#define SIZE 10

  

template <class X>

class stack

{

 X *arr;

 int top;

 int capacity;

  

public:

 stack(int size = SIZE); 

  

 void push(X);

 X pop();

 X peek();

  

 int size();

 bool isEmpty();

 bool isFull();

  

 ~stack() {

 delete[] arr;

 }

};

  

template <class X>

stack<X>::stack(int size)

{

 arr = new X[size];

 capacity = size;

 top = -1;

}

  
  

template <class X>

void stack<X>::push(X x)

{

 if (isFull())

 {

 cout << "Overflow\nProgram Terminated\n";

 exit(EXIT_FAILURE);

 }

  

 cout << "Inserting " << x << endl;

 arr[++top] = x;

}

  

template <class X>

X stack<X>::pop()

{

 if (isEmpty())

 {

 cout << "Underflow\nProgram Terminated\n";

 exit(EXIT_FAILURE);

 }

  

 cout << "Removing " << peek() << endl;

 return arr[top--];

}

  
  

template <class X>

X stack<X>::peek()

{

 if (!isEmpty()) {

 return arr[top];

 }

 else {

 exit(EXIT_FAILURE);

 }

}

  
  

template <class X>

int stack<X>::size() {

 return top + 1;

}

  
  

template <class X>

bool stack<X>::isEmpty() {

 return top == -1; 

}

template <class X>

bool stack<X>::isFull() {

 return top == capacity - 1; 

}

  

int main()

{

 stack<string> pt(2);

  

 pt.push("A");

 pt.push("B");

  

 pt.pop();

 pt.pop();

  

 pt.push("C");

  

 cout << "The top element is " << pt.peek() << endl;

  
  

 cout << "The stack size is " << pt.size() << endl;

  

 pt.pop();

 if (pt.isEmpty()) {

 cout << "The stack is empty\n";

 }

 else {

 cout << "The stack is not empty\n";

 }

  

 return 0;

}
```


### PROGRAM 27 :[EXCEPTION HANDLING](https://replit.com/@shivamkumar57/Programming#27_exception_handle.cpp)
---
```C++
#include<iostream>

#include<vector>

using namespace std;
int main() {

 vector<int> vec;

 vec.push_back(0); 

 vec.push_back(1); 
 try

 {

 vec.at(2); 

 }

 catch (exception& ex)

 {

 cout << "Exception occurred! Element at index 2 doesn't exist" << endl;

 }

 return 0;

}
```





