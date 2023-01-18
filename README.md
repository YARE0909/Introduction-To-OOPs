## C is a very popular language used for various things ranging from application development to game development

[A quick tutorial for C++](https://www.w3schools.com/cpp/default.asp)

# Features of C++
1. ### Object Oriented
	C++ is an Object Oriented Programming(OOP) language unlike its predecessor C. In OOP everything is treated as an object which can be created or destroyed. Using OOP also has other advantages like being able to use the concepts of: 
	- Classes
	- Objects
	- Encapsulation
	- Polymorphism
	- Inheritance
	- Abstraction
 2. ### Machine Independent
	C++ is not [platform independent](https://www.geeksforgeeks.org/writing-os-independent-code-cc/) but it is machine independent which means you can code with C++ on different OS but you cannot run the executable file genereated in one OS on another OS
3. ### High-Level Language
	C++ is a high level language which means it is easier for us humans to understand it as it is closely associated with the human-comprehensible English language
4. ### Dynamic Memory Allocation
	Many times, We are not aware in advance how much memory is needed to store particular information in a defined variable and the size of required memory can be determined at run time. So When the program executes in C++ then the variables are allocated the [dynamical heap space](https://www.geeksforgeeks.org/memory-layout-of-c-program/).
5. ### Memory Management
	-   C++ allows us to allocate the memory of a variable or an array in run time. This is known as [Dynamic Memory Allocation](https://www.geeksforgeeks.org/c-language-2-gq/dynamic-memory-allocation-gq/).
	-   In other programming languages such as Java the compiler automatically manages the memories allocated to variables. But this is not the case in C++.
	-   In C++, the memory must be de-allocated dynamically allocated memory manually after it is of no use.
	-   The allocation and deallocation of the memory can be done using the [new and delete operators](https://www.geeksforgeeks.org/new-and-delete-operators-in-cpp-for-dynamic-memory/) respectively.
6. ###  Simple
	It is a simple language in the sense that programs can be broken down into logical units and parts, has rich library support and has a variety of data types. Also, the Auto Keyword of C++ makes life easier.

# Basics of C++

## Installation
To use C++ you need 2 main things a code editor to write the code in and a compiler to convert the code into something the computer can understand and execute.
For now we can start with [VS Code](https://code.visualstudio.com/download) for the text editor and the [MinGW](https://www.msys2.org/) C++ compiler.
[Here is how to integrate VS Code with MinGW](https://code.visualstudio.com/docs/cpp/config-mingw). Alternatively you can also use [Visual Studio](https://visualstudio.microsoft.com/) to get an IDE(Integrated Developer Environment) which offers more features specific to development in C++. But IDEs are very heavy, takes up a lot of storage space and might not run on low end PCs. [You can install Visual Studio here.](https://visualstudio.microsoft.com/downloads/)

## Syntax
All C++ files have a .cpp extention. Once you are done with the installation of the [C++ compiler](https://www.msys2.org) and  [VS Code](https://code.visualstudio.com/download) (or [Visual Studio](https://visualstudio.microsoft.com)) go ahead and create a file called main.cpp and type in the following basic hello world program
```cpp
#include <iostream>
using namespace std;

int main(){
cout << "Hello World!;
return 0;
}
```
In the above example lets break it down:
1. First we have the header files. `#include <iostream>` is a header file library that lets us work with input and output objects. Header files add functionality to C++ programs.
2. The `int main()` function is the entry point into the C++ program which means whenever you run a C++ file it calls the `main()` function. This function is mandatory or else your program will not run.
3. Inside the `int main()` function are what we call statement. A statement is a line of code or instruction to be executed by the computer. `cout << "Hello World";` and `return 0;` are statements.
4. In C++ like in C every statement is terminated by the semi colon(`;`) character. This character tells  the compiler where one line ends and another one starts as C++ ignores white spaces.
5. Every `(), [] and {}` must be closed in C++.

## Variables
Variables are containers for storing data values. In C++ there are different types of variables with different data types. For example:
-   `int` - stores integers (whole numbers), without decimals, such as 123 or -123
-   `double` - stores floating point numbers, with decimals, such as 19.99 or -19.99
-   `char` - stores single characters, such as 'a' or 'B'. Char values are surrounded by single quotes
-   `string` - stores text, such as "Hello World". String values are surrounded by double quotes
-   `bool` - stores values with two states: true or false
### Declaring variables
#### Syntax
`dataType variableName = value;`
#### Example
```cpp
int num = 69;
```
You can also declare a variable without assigning the value, and assign the value later:
```cpp
int myNum;  
myNum = 15;  
```

## Data Types
A data type is a classification that specifies which type of value a variable has and what type of mathematical, relational or logical operations can be applied to it without causing an error.
There are 3 types of data types in C++:
1. ### Primitive Data Types
	These data types are built-in or predefined data types and can be used directly by the user to declare variables. Primitive data types available in C++ are:
	-   Integer
	-   Character
	-   Boolean
	-   Floating Point
	-   Double Floating Point
	-   Valueless or Void
	-   Wide Character
2. ### Derived Data Types
	Derived data types that are derived from the primitive or built-in datatypes are referred to as Derived Data Types. These can be of four types namely:
	-   Function
	-   Array
	-   Pointer
	-   Reference
3. ### User Defined Data Type:
	User defined data types are defined by the user itself. Like, defining a class in C++ or a structure. C++ provides the following user-defined datatypes
	-   Class
	-   Structure
	-   Union
	-   Enumeration
	-   Typedef defined Datatype
### Data Type Modifiers
Datatype modifiers are used with built-in data types to modify the length of data that a particular data type can hold.Data type modifiers available in C++ are: 
-   Signed
-  Unsigned
-   Short
-   Long