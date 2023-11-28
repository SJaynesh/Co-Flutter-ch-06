# OOP (Object Oriented Programming) 

<br><br>  

### (6.1) 

<br><br>

## Function as Expression :

<br>

### Function :
> * `A re - usable block of code is called a function.`
> * re - usable block of code which can be accessed any time just by calling through its name.
> * Function are used to divide a large dart program into smaller pieces.
> * function can be denoted by '()'.
> * function also called procedure or subroutine.

<br><br>

### Types of function block :
> * 1. block function    () {}   //Can contain multiple statements
> * 2. lambda function   () =>   //Can contain only single statement (Expression)

### Types of Function : 

> `1) Built - in function` <br><br>
> `2) User Defined Functions (UDF) `

<br><br>

### 1) Built - in function :

<br>

> * Functions that are already created are called built in functions.
> * Built-in function is a function that is provided by the dart standard library.
> * print(), int.parse(), double.parse(), readLineSync() , ...


### 2) User Defined Functions (UDF) : 

<br>

> * A user-defined function is a function that you create yourself to perform a specific task within your C program.

<br><br>

#### Life cycle of function :

##### `1. Declaration` (Register) 
##### `2. Definition` (Put Logic) 
##### `3. Calling` (Use) 

<br><br>

### Types : 
  > 1) TNRN (Take Nothing Return Nothing) 
  > 2) TSRN (Take Something Return Nothing) 
  > 3) TNRS (Take Nothing Return Something) 
  > 4) TSRS (Take Something Return Something) 

<br><br>

### Syntax : 
<br>

<pre>
  ReturnDatatype functionName([argument])
  {
	  [statement] / [return value]
  }


*  [ ] : means Optional.

* ReturnDatatype :
  
    - If returns => int , char , float…
  
    - According to the return value.
  
    - If does not return => void



</pre>

<br><br>

## 1) TNRN (Take Nothing Return Nothing) : 

<br>

> * `Function is not get an argument and does not return any data type.`



<pre>
  // Defining an UDF :

  void functionName()
  {
      // Function body;
  }

  // Calling an UDF :
  
  functionName();
  
</pre>

<br>

## 2) TSRN (Take Something Return Nothing) : 

<br>

> * `Function is get an argument and does not return any data type.`

<pre>
  // Defining an UDF :

  void functionName(parameters)
  {
      // Function body;
  }

  // Calling an UDF :
  
  functionName(arguments);
  
</pre>

<br>

## 3) TNRS (Take Nothing Return Something) :

<br>

> * `Function is not get an argument and return any data type.`

<pre>
  // Defining an UDF :

  return-type functionName()
  {
      // Function body;
        return something;
  }

  // Calling an UDF :
  
  var variable_name = functionName();
  
</pre>

<br>

## 4) TSRS (Take Something Return Something) : 

<br>

> * `Function is get an argument and return any data type.`

<pre>
 // Defining an UDF :

  return-type functionName(parameters)
  {
      // Function body;
        return something;
  }

  // Calling an UDF :
  
  var variable_name = functionName(arguments);
  
</pre>

<br><br>

## Expression :
> * `Expression means Single line Statement.`

<br>

## Function as Expression :
> * `Function as expression means converting a function into short-hand syntax.`
> * function which contains only single statement.
> * Fat-arrow (=>) is used to make any function look like an expression.

### Steps to convert into expression :
> * remove '{}' or 'return' keyword.
> * add '=>' (fat arrow) in replacement of '{}' and 'return' keyword.
> * A function that has a body of only one line, in the function itself expression can be converted. For that { } has to be removed.
> * Fat arrow can work as a return keyword.  

<br>

#### Example - Simple
<pre>
	void name() {
	
		print("Hello Dart");

	}
</pre>

<br>

#### Example - Converting into Expression
<pre>
	void name() => print("Hello Dart");
</pre>

<br>

### Note : `If any function has return statement then also remove return keyword from it is necessary.`

<br>

#### Example - Simple
<pre>
	int sum(int a, int b) {
	
		return a + b;

	}
</pre>

<br>

#### Example - Converting into Expression
<pre>
	int sum(int a , int b) => a + b;
</pre>

<br><br>


## Types of Function Parameters :

<br>

> * `While defining a function, catch parameters can be defined in 3 different ways.`

<br>

> * i) Default Parameters
> * ii) Optional Parameters
> * iii) Required Parameters 

<br><br>

### 1) `Default Parameters`

<br>

<pre>
	import 'dart:io';

	int sum(int a, int b) => a+b;

	void main() {

		int a,b,res;

		stdout.write("Enter a : ");
		a = int.parse(stdin.readLineSync()!);

		stdout.write("Enter b : ");
		b = int.parse(stdin.readLineSync()!);

		res = sum(a,b);

		print("😀 Sum of $a and $b = $res 😀");
	}
</pre>

<br><br>

### 2) `Optional Parameters`

<br>

> * Optional Parameters Two Types :

> * 1) Optional Positional
> * 2) Optional Named


### 1) Optional Positional :
> * To specify optional positional parameters, use square [ ] brackets.
> *  Optional Positional to assign default value/null aware.
> *  ?? (NULL CHECK OPERATOR)

#### Syntax :
> * `void functionName(param1, [optional_param_1, optional_param_2]) { }`

<pre>
	// Optional Positional <=> []
	
	int sum(int a, int b, [int c = 0, int d = 0]) => a + b + c + d;
	
	void main() {
	  int res = sum(10, 10, 10, 10);
	
	  print("Sum : $res");
	}

</pre>

<br>

<pre>
	// Optional Positional <=> []
	
	int sum(int a, int b, [int? c, int? d]) => a + b + (c ?? 0) + (d ?? 0);
	void main() {
	  int res = sum(10, 10);
	
	  print("Sum : $res");
	}

</pre>

<br><br>

### 2) Optional Named :
> * Unlike positional parameters, the parameter's name must be specified while the value is being passed.
> * Curly brace { } can be used to specify optional named parameters.
> * Optional Named to assign default value/null aware/required.

<br>

<pre>
	int sum(int a, int b, {int c = 0, int d = 0}) => a + b + c + d;
	
	void main() {
	  int res = sum(10, 20, c: 50, d: 40);
	  print("Sum : $res");
	}

</pre>


<br><br>

### 3) `Required Parameters :`
> * Required Parameters is use required keyword.
> * Required means Fix assign arguments in function.
> * required arguments to write inside for { }.

<pre>
	
int sum(int a, int b, {required int c, required int d}) => a + b + c + d;

void main() {
  int res = sum(10, 20, c: 10, d: 20);

  print("Sum : $res");
}

</pre>

<br><br>

### (6.2)

<br><br>

## OOP :
> * `OOP Stander for Object Oriented Programming.`
> * OOP is a Concept by which code becomes well structured, well Organized, well Secured and increases it's reusability.

<br>

### Why use OOP concept ?

<br>

> * You code is :-
> * - Well Structured
> * - Well Organuzed
> * - Well Secured
> * - Reusability

<br/><br/>

### - Principles of OOP :

<br>


> * 4 Principles OOP :
>
>   * 1. Encapsulation => Data binding => (To Wrap)
>   * 2. Inheritence => Data passing  => (to share)
>   * 3. Polymorphism => Multitasking => (to behave in multiple ways)
>   * 4. Data Abstraction => Security/Restriction => (to secure)

<br/><br/>

<p><img src = "https://github.com/SJaynesh/Co-Flutter-ch-06/assets/115562979/f131c9bd-27bf-454f-9721-66d953e4d0ec.png" width=60% height=50%></p>

<br>

https://github.com/SJaynesh/CPP-Languge-Ch-02/assets/115562979/62b1204a-2cb5-4d72-88d5-1b70ce6103b8

<br/><br/>

### Two components of OOP :

<br>

 > `Class` <br/>
 > `Object` <br/>

<br/><br/>

## Class & Object :

<br>

### Class :

<br>

> * `Class is a Collection of Data Members And Data Member Function.`
> * Class is a User Define Datatype.
> * Class is a Categorized Collection of Attributes and methods.
> * Class is a blueprint which is being followed by its variables(objects).

<br>

### Object :

<br>

> * Object is a Variable(instance) of class by which we can use the data of class.
> * Object is reference of pre-built category(class) which provides the inbuilt function alities.

<br>

<p><img src = "https://github.com/SJaynesh/Co-Flutter-ch-06/assets/115562979/7db99bc9-ab03-4ee2-a7a7-a7a6d4aa8513.png" width=60% height=50%></p>

<br>

<p><img src = "https://github.com/SJaynesh/Co-Flutter-ch-06/assets/115562979/fb2259ea-6fdf-4a8c-ad25-94ebaa12f3f8.png" width=60% height=50%></p>

<br>

https://github.com/SJaynesh/CPP-Languge-Ch-02/assets/115562979/8cd02d9c-bc67-4177-95f6-a3ebf182743f

<br><br>

## Syntax :

<br>

<pre>
	* Syntax to declare a class :
	
	class ClassName
	{
		/*
		Properties;
		Methods;
		Constructors;
		*/
	}

	* Syntax to create an object:
	void main()
	{
		ClassName object_name = ClassName();
	}
	
</pre>

<br><br>

## Encapsulation :

<br>

> * Encapsulation means wrapping code as much as you can in a class.
> * Every logic must be written in class.
> * It helps in hiding the implementation details and provides data protection.

<br>

### Setter And Getter

<br>

> * Getter and Setter are the special methods of the class, which can be used to assign and get the values of the properties of the class.

<br>

#### Setter :

<br>

> * Setter method is used to assign or initialise properties of a class.
> * A function to take input of attributes in class.

<br>

#### Getter :

<br>

> * A getter method is used to access the properties of a class.
> * A function to give output of attributes in class.

<br><br>

<pre>
	import 'dart:io';
	
	// Class
	class Student {
	  int? rollNo;
	  String? name;
	  double? per;
	
	  // Setter
	  void setData() {
	    stdout.write("Enter your Roll No : ");
	    rollNo = int.parse(stdin.readLineSync()!);
	    stdout.write("Enter your Name : ");
	    name = stdin.readLineSync()!;
	    stdout.write("Enter your Percentage  : ");
	    per = double.parse(stdin.readLineSync()!);
	  }
	
	  // Getter
	  void getData() {
	    print("Roll No\t: $rollNo");
	    print("Name\t: $name");
	    print("Per\t: $per");
	  }
	}
	
	void main() {
	
	  //Object
	  Student s = Student();
	
	  s.setData();
	  s.getData();
	}

</pre>

<br><br>

## this keyword :

<br>

> * When class attributes and function parameters both have same name, then we can make difference and identify the class attributes using this keyword.
> * this keyword is written before the class variable.

<br>

<pre>
	// Class
	class Student {
	  int? id;
	  String? name;
	  double? per;
	
	  //Setter
	  // This Keyword
	  void setData({required int id, required String name, required double per}) {
	    this.id = id;
	    this.name = name;
	    this.per = per;
	  }
	
	  //Getter
	  void getData() {
	    print("Roll No\t: $id");
	    print("Name\t: $name");
	    print("Per\t: $per");
	  }
	}
	
	void main() {
	  //Object
	  Student s = Student();
	
	  s.setData(id: 101, name: "Jaynesh", per: 80.56);
	
	  s.getData();
	}

</pre>

<br><br>

## Array of Objects : 

<br>

> * Collection / group of Object of same class.

<br>

<pre>
	import 'dart:io';

	// Class
	class Student {
	  int? rollNo;
	  String? name;
	  double? per;
	
	  // Setter
	  void setData() {
	    stdout.write("\nEnter your Roll No : ");
	    rollNo = int.parse(stdin.readLineSync()!);
	    stdout.write("Enter your Name : ");
	    name = stdin.readLineSync()!;
	    stdout.write("Enter your Percentage  : ");
	    per = double.parse(stdin.readLineSync()!);
	  }
	
	  // Getter
	  void getData() {
	    print("\nRoll No\t: $rollNo");
	    print("Name\t: $name");
	    print("Per\t: $per");
	  }
	}
	
	void main() {
	  int n;
	
	  stdout.write("Enter n : ");
	  n = int.parse(stdin.readLineSync()!);
	
	  // Array Of Object
	  List obj = List.generate(n, (index) => Student());
	
	  obj.forEach((e) {
	    e.setData();
	  });
	
	  obj.forEach((e) {
	    e.getData();
	  });
	}

</pre>


<br><br>

### (6.3)

<br>


## Custom setters and getters :






