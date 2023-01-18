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
To use C++ you need 2 main components a code editor to write the code in and a compiler to convert the code into something the computer can understand and execute.
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
```
Hello World
```
In the above example lets break it down:
1. First we have the header files. `#include <iostream>` is a header file library that lets us work with input and output objects. Header files add functionality to C++ programs.
2. The `int main()` function is the entry point into the C++ program which means whenever you run a C++ file it calls the `main()` function. This function is mandatory or else your program will not run.
3. Inside the `int main()` function are what we call statement. A statement is a line of code or instruction to be executed by the computer. `cout << "Hello World";` and `return 0;` are statements.
4. In C++ like in C every statement is terminated by the semi colon(`;`) character. This character tells  the compiler where one line ends and another one starts as C++ ignores white spaces.
5. Every `(), [] and {}` must be closed in C++.

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
### Type Conversion
A type cast/type conversion is basically a conversion from one type to another. There are two types of type conversion:
1. **Implicit Type Conversion**
	- Also known as automatic type conversion.
	-   Done by the compiler on its own, without any external trigger from the user.
	-   Generally takes place when in an expression more than one data type is present. In such condition type conversion (type promotion) takes place to avoid lose of data.
	-   All the data types of the variables are upgraded to the data type of the variable with largest data type.
	- It is possible for implicit conversions to lose information, signs can be lost (when signed is implicitly converted to unsigned), and overflow can occur (when long long is implicitly converted to float).
		**Example**
		```cpp
		#include <iostream>
		using namespace std;
		
		int main()
		{
			int x = 10; // integer x
			char y = 'a'; // character c
		
			// y implicitly converted to int. ASCII
			// value of 'a' is 97
			x = x + y;
		
			// x is implicitly converted to float
			float z = x + 1.0;
		
			cout << "x = " << x << endl
				<< "y = " << y << endl
				<< "z = " << z << endl;
		
			return 0;
		}
		```
		```
		x = 107
		y = a
		z = 108
		```
2. **Explicit Type Conversion**
	This process is also called type casting and it is user-defined. Here the user can typecast the result to make it of a particular data type. In C++, it can be done by two ways:
	- **Converting by assignment:** This is done by explicitly defining the required type in front of the expression in parenthesis. This can be also considered as forceful casting.
		**Syntax**
		`(type) expression`
		**Example**
		```cpp
		#include <iostream>
		using namespace std;

		int main()
		{
			double x = 1.2;
		
			// Explicit conversion from double to int
			int sum = (int)x + 1;
		
			cout << "Sum = " << sum;
		
			return 0;
		}
		```
		```
		Sum = 2
		```
	- **Conversion using Cast operator:** A Cast operator is an **unary operator** which forces one data type to be converted into another data type.  
	C++ supports four types of casting:
	
	1.  [Static Cast](https://www.geeksforgeeks.org/static_cast-in-c-type-casting-operators/)
	2.  Dynamic Cast
	3.  [Const Cast](https://www.geeksforgeeks.org/casting-operators-in-c-set-1-const_cast/)
	4.  [Reinterpret Cast](https://www.geeksforgeeks.org/reinterpret_cast-in-cpp/)
	
	**Example:**
	```cpp

	#include <iostream>
	
	using namespace std;
	
	int main()
	{
	    float f = 3.5;
	    // using cast operator
	    int b = static_cast<int>(f);	
	    cout << b;
	}
	```
	
	`3`

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
There are 3 types of variables in C++:
1.  **Local Variables**
	- A variable defined within a block or method or constructor is called a local variable. 
    -   These variables are created when entered into the block or the function is called and destroyed after exiting from the block or when the call returns from the function.
    -   The scope of these variables exists only within the block in which the variable is declared. i.e. we can access this variable only within that block.
    -   Initialization of Local Variable is Mandatory.
3.  **Instance Variables**
	- Instance variables are non-static variables and are declared in a class outside any method, constructor, or block. 
    -   As instance variables are declared in a class, these variables are created when an object of the class is created and destroyed when the object is destroyed.
    -   Unlike local variables, we may use access specifiers for instance variables. If we do not specify any access specifier then the default access specifier will be used.
    -   Initialization of Instance Variable is not Mandatory.
    -   Instance Variable can be accessed only by creating objects.
5.  **Static Variables**
	- Static variables are also known as Class variables. 
    -   These variables are declared similarly as instance variables, the difference is that static variables are declared using the static keyword within a class outside any method constructor or block.
    -   Unlike instance variables, we can only have one copy of a static variable per class irrespective of how many objects we create.
    -   Static variables are created at the start of program execution and destroyed automatically when execution ends.
    -   Initialization of Static Variable is not Mandatory. Its default value is 0
    -   If we access the static variable like the Instance variable (through an object), the compiler will show the warning message and it won’t halt the program. The compiler will replace the object name with the class name automatically.
    -   If we access the static variable without the class name, the Compiler will automatically append the class name.
#### Constants
Constants are identifiers with a value which can not be changed once assigned. When you do not want to change existing variable values, use the `const` keyword. Constants are unchangeable and read-only.
**Syntax**
`const dataType variableName = value;`
**Example**
```cpp
const int PI = 3.14; // The value of the PI variable will always be 3.14
PI = 3; // This will return an error
```
#### Pointer
Pointers are symbolic representations of addresses. They enable programs to simulate call-by-reference as well as to create and manipulate dynamic data structures. Iterating over elements in arrays or other data structures is one of the main use of pointers. 
The address of the variable you’re working with is assigned to the pointer variable that points to the same data type. [Click here for more information on pointers](https://www.geeksforgeeks.org/cpp-pointers/)
**Syntax**
```
datatype *variableName;
```
**Example**
```cpp
int *ptr;
```

## Operators
Operators are used to perform operations on variables and values. C++ divides the operators into the following groups:

1. **Arithmetic operators**
	Arithmetic operators are used to perform common mathematical operations.
	`+` - Adds two values
	`-` -Subtracts one value from another
	`*` - Multiplies two values
	`/` - Divides one value by another
	`%` - Returns the division remainder
	`++` - Increases the value of a variable by 1
	`--` - Decreases the value of a variable by 1
2. **Assignment operators**
	Assignment operators are used to assign values to variables.
	`=` - Used to assign a value to something
	`+=` - Adds the RHS value before assigning the value
	`-=` - Subtracts the RHS value before assigning the value
	`*=` - Multiplies the RHS value before assigining the value
	`/=` - Divides the LHS value by the RHS value before assigning the value
	`%=` - Assigns the remainder of the value after divinding the LHS by the RHS
3. **Comparison operators**
	Comparison operators are used to compare two values (or variables). This is important in programming, because it helps us to find answers and make decisions. The return value of a comparison is either `1` or `0`, which means **true** (1) or **false** (0).
	`==` - Equal to
	`!=` - Not equal to
	`>` - Greater than
	`<` - Lesser than
	`>=` - Greater than or equal to
	`<=` - Lesser than or equal to
4. **Logical operators**
	Logical operators are used to determine the logic between variables or values
	`&&` - Logical and
	`||` - Logical or
	`!` - Logical not
5. **Bitwise operators**
	-  The **& (bitwise AND)** in C or C++ takes two numbers as operands and does AND on every bit of two numbers. The result of AND is 1 only if both bits are 1.  
	-  The **| (bitwise OR)** in C or C++ takes two numbers as operands and does OR on every bit of two numbers. The result of OR is 1 if any of the two bits is 1. 
	-  The **^ (bitwise XOR)** in C or C++ takes two numbers as operands and does XOR on every bit of two numbers. The result of XOR is 1 if the two bits are different. 
	-  The **<< (left shift)** in C or C++ takes two numbers, left shifts the bits of the first operand, the second operand decides the number of places to shift. 
	-  The **>> (right shift)** in C or C++ takes two numbers, right shifts the bits of the first operand, the second operand decides the number of places to shift. 
	-  The **~ (bitwise NOT)** in C or C++ takes one number and inverts all bits of it.


## Input And Output
Input and output is how you take data from and display data to the user.

### Output
`cout` is a predefined variable that displays data to the user on the monitor with the `<<` operator
#### Syntax
`cout << string;`
#### Example
```cpp
cout << "Hello World";
```
```
Hello World
```

### Input
`cin` is a predefined variable that reads data from the keyboard with the extraction operator(`>>`).
##### Syntax
`cin >> variableName;`
##### Example
```cpp
int x;
cout << "Enter a number: ";
cin >> x;
cout << "The number you have entered is: " << x;
```
```
Enter a number: 69
The number you have entered is: 69
```

## Conditional Statements
