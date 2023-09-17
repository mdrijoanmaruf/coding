# C++ Fundamental Notes

## Varibale:
``` c++
int a = 100;
double b = 200;
string c = "Md Rijoan Maruf"
```

## Comments:
```c++
// This is single line comments
/* This is multi line
comments*/
```
## Varialbe Scop:
### Local Variable:
* Inside any function variable
### Global Variable:
* Outside any function variable

## Data Type:
* int , float , char , duble , bool
* strct , union 
* Array , Pointer , Function

## Basic Input / Output:
``` c++
cout << "Hello Worls!" << endl ; // Output function
int a ;
cin >> a;                        // Input function
```
## Operators:
* **Arithmetic** : + , - , * , / , % , ++ , -- 
* **Assignment** : = , += , -= , /= , *= 
* **Comparison** : == , != , > , < , >= , <=
* **Logical** : && , || , !

## Reference Variable:
* Defines another name for an already existing variable
```c++
int x = 100;
int& y = x;     // y is another name of x
cout << x << endl;      // 100
cout << y << endl;      // 100
                        // endl --> prints new line
```
## Constant:
* Constant is unchangeable
```c++
const x = 100
```
## Manipulator:
```c++
endl    // Print new line
setw    // Specify the width
cout << setw(6) << 5 << endl;
        // .....5
```
## Operator Precedence:
* **1st** : * , / , %
* **2nd** : + , - etc.

## Control Structures:

**If-Else**
```c++
int i = 10;
if(i > 100){
    // code to execute
}
else if i > 20{
    // code to execute
}
else{
    // code to execute
}
```

**Switch**
```c++
switch (age){
    case 18:
    // code
        break;
    case 19:
    // code
        break;
    case 20:
    // code
        break;
    default:
    //code
        break;
}
```

## Loop:
**While Loop**
```c++
while(i < 100){
    cout << i << endl;
    i ++
}
```
**DO While Loop**
```c++
do{
    cout << i << endl;
    i ++
}while(i < 100)
```
**For Loop**
```c++
for(int i = 0; i < 100 ; i++){
    cout << i << endl;
}
```

## Break & Continue:
```c++
break;      // jump out of a loop
continue;   // Breaks one loop
```
## Pointers:
Store a address of a variable.
```c++
int x = 10;         // Store 10
int* y = &x;        // Store address of x

cout << x << endl;  // 10
cout << *y << endl; // 10

cout << y << endl;  // address location of x
cout << &x << endl; // address location of x
```
## Arrays:
**Array**
```c++
int marks[3] = {12, 34, 56}
cout << marks[0]    // 12
                    // index start with zero
```
**Array Pointer**
```c++
int marks[3] = {12, 34, 56}
int* p = marks;
cout << *p ;        // 12
cout << *(p+1) ;    // 34
```
## Structures:
```c++
struct employee{
    int id;
    int salary;
};

int main(){
    struct employee = saif;
    saif.id = 100;
    saif.salary = 2000;
}
```

**typedef**
```c++
typedef struct employee{
    int id;
    int salary;
}ep;

int main(){
    ep saif;      // ep --> struct employee
    saif.id = 100;
    saif.salary = 2000;
}
```

## Unions:
```c++
union money{
    int Bkash;
    int cash;
};

int main(){
    union money m1;
    m1.Bkash = 10000;
    m1.cash = 100;
}
```

## Enumeration:
```c++
enum season { spring, summer, autumn, winter };
enum season 
{   spring = 0, 
    summer = 4, 
    autumn = 8,
    winter = 12
};
```
## Functions:
```c++
int sum(int a , int b){
    return a + b;
}

int main(){
    x = sum(10, 20);     // x will 30
}
```
**Call by value**
```c++
void swap(int a , int b){
    int temp = a;
    a = b;
    b = temp;
}

int main(){
    int a , b = 10 , 30;
    swap(a, b);       // can't swap this number
}
```
**Call by reference**
```c++
void swap(int *a , int *b){
    int temp = *a;
    *a = *b;
    *b = *temp;
}

int main(){
    int a , b = 10 , 30;
    swap(&a, &b);       // will swap this number because a, b will reference variable of a, b
}
```
**Call by Reference Variable**
```c++
void swap(int &a , int &b){
    int temp = a;
    a = b;
    b = temp;
}

int main(){
    int a , b = 10 , 30;
    swap(a, b);       // will swap this number because a, b will reference variable of a, b
}
```

**Inline Function**
```c++
inline int product(int a , int b){
    return a * b;
}
// Used to reduce function call
```
**Default Argument**
```c++
int money(int m , int rate = 2){    // rate is default value and it can be changed
    return m*rate;
}                                   // it can called with one value
```
**Constant Argument**
```c++
int strp(const int x){  // x is unchangeble    
    cout << "Value : " << x << endl;
}                                   
```
## Recursion & Recursive Function:
when a function call itself it called recursion.
```c++
int factorial(int n){
    if(n <= 1){
        return 1;
    }
    else{
        return n*factorial(n - 1)   // call itself until n <= 1
    }
}
```
**Function Overloading**
```c++
int sum(int a , int b){     // function 1
    return a + b;
}
int sum(int a , int b , int c){     // function 2
    return a + b + c;
}
// sum() function can be called with 2 or 3 argument
int main(){
    sum(10 , 20);           // execute function 1
    sum(20 , 20 , 30)       // execute function 2
}
```
## Object Oriented Programming (OOP):
**Classes private and public**
```c++
class Emp{          // create a new call name is emp
    private:        // default value
    int a , b , c;  // attribute int
    int s;          // attribute string
    public:
    int d , c;
}
```
**Classes Function / Methods**
```c++
class Emp{      
    public:
    int a, b, c;
    void getdata(){
        cout << a;
    }
}

int main(){
    Emp saif;   // create a new object name : saif
    saif.getdata();
}
```
**Classes Inside method/function**
``` c++
class myclass{
    public:
    void mymethod(){
        cout << "Hello World" << endl;
    }
};
int main(){
    myclass myobj;
    myboj.mymethod();
}
```

**Classes Outside method/function**
``` c++
class myclass{
    public:
    void mymethod();
};
void myclass::mymethod(){
    cout << "Hello World"<< endl;
}
int main(){
    myclass myobj;
    myboj.mymethod();
}
```

**Nestion of member function**:
Call a function in a function

**Object Memory Alucation**:
The memory is only allocated to the variable of the calss when the object is created.

**Array in callses**:
* at() --> Access element of array
* get() --> Input array element

```c++
class shop{
    int item[100];
    int price[100];
    public:
    void set_price(void){
        // code
    }
}
```
