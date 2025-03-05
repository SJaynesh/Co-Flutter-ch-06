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

<br>

> * 1. block function    () {}   //Can contain multiple statements
> * 2. lambda function   () =>   //Can contain only single statement (Expression)

### Types of Function : 

<br>

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

<br>

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

<br>


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

<br>

> * `Expression means Single line Statement.`

<br>

## Function as Expression :

<br>

> * `Function as expression means converting a function into short-hand syntax.`
> * function which contains only single statement.
> * Fat-arrow (=>) is used to make any function look like an expression.

<br>

### Steps to convert into expression :

<br>

> * remove '{}' or 'return' keyword.
> * add '=>' (fat arrow) in replacement of '{}' and 'return' keyword.
> * A function that has a body of only one line, in the function itself expression can be converted. For that { } has to be removed.
> * Fat arrow can work as a return keyword.  

<br>

#### Example - Simple
<br>

<pre>
	void name() {
	
		print("Hello Dart");

	}
</pre>

<br>

#### Example - Converting into Expression

<br>

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

<br>

### 1) Optional Positional :

<br>

> * To specify optional positional parameters, use square [ ] brackets.
> *  Optional Positional to assign default value/null aware.
> *  ?? (NULL CHECK OPERATOR)

#### Syntax :

<br>

> * `void functionName(param1, [optional_param_1, optional_param_2]) { }`

<br>

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

<br>

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

<br>

> * Required Parameters is use required keyword.
> * Required means Fix assign arguments in function.
> * required arguments to write inside for { }.

<br>

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

<br>

>* `Custom Setter and Getter is a updated version in setter and getter.`
>* Custom setter and getter are used when attributors are private and need to be accessed.
>* set and get keyword are used to become custom centers and getters.

<br>

### How to create a Private attributes in class ?

<br>

> * 1. Class must be created in separate dart file.
> * 2. Put underscore '_' before private members. 


#### Example :

<br>

<pre>
	int? _id;
	String? _name;
</pre>

<br>

<pre>
  Student.dart

class Student {
  int? _id;
  String? _name;
  double? _per;

  void setData({required int id, required String name, required double per}) {
    this._id = id;
    this._name = name;
    this._per = per;
  }

  void getData() {
    print("Id\t: $_id");
    print("Name\t: $_name");
    print("Per\t: $_per");
  }
}

</pre>

<br>

<pre>
 Student_main.dart
	
import 'Student.dart';

void main() {
  Student obj = Student();

  obj.setData(id: 101, name: "Jaynesh", per: 89.63);
  obj.getData();
}

</pre>

<br><br>

## Custom Setter and Getter:

<br>

> * must be created for each attribute separately.

<br>

### Custom Setter :

<br>

#### Syntax :
<pre>
	set field_name(argument)
	{
	 // Statement
	}
</pre>

<br>

### Custom Getter :

<br>

#### Syntax :
<pre>
	return_type get field_name
	{
	 // return val;
	}
</pre>

<br>


<pre>
Student.dart
	
class Student {
  int? _id;
  String? _name;
  double? _per;

  set setId(int id) {
    _id = id;
  }

  set setName(String name) {
    _name = name;
  }

  set setPer(double per) {
    _per = per;
  }

  int get getId {
    return _id!;
  }

  String get getName {
    return _name!;
  }

  double get getPer {
    return _per!;
  }
}

</pre>


<pre>
Student_main.dart
import 'Student_custom_setter_getter.dart';

void main() {
  Student obj = Student();

  obj.setId = 101;
  obj.setName = "Jaynesh";
  obj.setPer = 89.65;

  print("ID: ${obj.getId}");
  print("Name: ${obj.getName}");
  print("Per: ${obj.getPer}");
}

</pre>

<br><br>

## Cascade Operator (..) :

<br>

> * To access multiple attribute or methods at same time.
> * can be denoted with '..'

<br>

<pre>
import 'dart:io';

class Car {
  int? model_no;
  String? model_name;
  String? color;

  void inputCarAtributes() {
    stdout.write("Enter car model number: ");
    model_no = int.parse(stdin.readLineSync()!);
    stdout.write("Enter car model number: ");
    model_name = stdin.readLineSync()!;
    stdout.write("Enter car model number: ");
    color = stdin.readLineSync()!;
  }

  void outputCarAtributes() {
    print("Car Model Number : $model_no");
    print("Car Model Name : $model_name");
    print("Car Model Color : $color");
  }
}

void main() {
  Car car = Car();

  //cascade operator
  car
    ..inputCarAtributes()
    ..outputCarAtributes();
}

</pre>

<br><br>

## Constructor & Its types :

<br>

> * `Constructor is a block of code which is automatically invoked when class is instanciated.`
> * Constructor is automatically called when an object(instance of class) is created. It is a special member function of the class.
> * It mainly used to assign data in attributes.

<br>

<pre>

	- To instanciate => To create Object
	- To invoke  => To execute any method of class
	- To call => To execute an UDF
</pre>

<br>

### Rules to Create Constructor :

<br>

> * The name constructor must be same as class name.
> * Constructor cannot have any return datatype like void, int, double, etc...
> * It cannot return anything(Value).

<br/><br/>

https://github.com/SJaynesh/CPP-Languge-Ch-04/assets/115562979/45f31973-7713-4d2c-9c58-6a1c581e41f5

<br/><br/>

<pre>
class DartProgram {
  DartProgram() {
    print("Hello Dart Language 😀");
  }
}

void main() {
  DartProgram dartProgram = DartProgram();
}
</pre>

<br><br>

## Types of Constructor :

<br>

> * 1. Default Constructor.
> * 2. Parameterized Constructor.
> * 3. Named Constructor.
> * 4. Factory Constructor.

<br> 

### 1. Default Constructor:

<br>

#### `Syntax :`

<br>

<pre>
	class_name() {
		// constructor body
	}
</pre>	

<br>

### 2. Parameterized Constructor:

<br>

#### `Syntax :`

<br>

<pre>
	class_name(parameteres) {
		// constructor body
	}
</pre>	

<br>

#### `Example :`

<br>

<pre>
class Data {
  int? no;
  String? name;

  // Parameterized Constructor
  Data({required int no, required String name}) {
    this.no = no;
    this.name = name;
  }

  //getter
  void output() {
    print("No\t: $no");
    print("Name\t: $name");
  }
}

void main() {
  Data data = Data(no: 6060, name: "Sarkar");

  data.output();
}
</pre>

<br>

### `Note:` In dart, we cannot create both default and parameterised constructor in same class. So for this solution, dart provides named constructor.


### 3. Named Constructor:

> * A Named constructor is used to create more than one constructor.

<br>

#### `Syntax :`

<br>

<pre>
	class_name.constructor_name(parameteres) {
		// constructor body
	}
</pre>	

<br>

#### `Example :`

<br>

<pre>
import 'dart:io';

class Student {
  int? id;
  String? name;

  Student() {
    print("Default Constructor");
  }

  Student.getInstence() {
    print("object created..");
  }

  Student.setValue() {
    stdout.write("Enter No: ");
    id = int.parse(stdin.readLineSync()!);

    stdout.write("Enter Name: ");
    name = stdin.readLineSync()!;
  }
}

void main() {
  Student student = Student();
  Student student1 = Student.getInstence();
  Student student2 = Student.setValue();
}

</pre>

<br><br>

### How to provide attributes in a class?

<br>

#### 1. Null Safety:
> * Attributors can also be made null.
> * `Ex.` int? id;

<br>

### 2.Late Keyword:
> * we use the late keyword to declare variables that will be initialized later.
> * `Ex.` late int id;

<br>

#### 3. Final Keyword:
> * final to fix the value.
> * When we final the variable we don't need to assign the value to the variable.
> * `Ex.` final int id;

<br>

#### 4. Default Value:
> * Atributes to assign default value.
> * `Ex.` int id = 0;

<br><br>


### (6.4)

<br>

## Factory constructor:

<br>

> * Factory constructor to convert raw data into objects.
> * Factory constructor return the current class's object.
> * Factory constructor can be created using 'factory' keyword.
> * `A factory constructor is convert  raw data into objects and returns an object of the current class.`
> * A constructor that takes a map in its parameters and returns an object is called a factory constructor.


<br>

<pre>
class Student {
  final int id;
  final String name;
  final double per;

  Student({required this.id, required this.name, required this.per}) {
    print("Object Created");
  }

  factory Student.fromMap({required Map data}) {
    return Student(
      id: data['id'],
      name: data['name'],
      per: data['per'],
    );
  }

  void getData() {
    print("ID\t: $id");
    print("NAME\t: $name");
    print("PER\t: $per");
  }
}

void main() {
  Map stud = {
    'id': 101,
    'name': "Jaynesh Sarkar",
    'per': 89.56,
  };

  Student student = Student.fromMap(data: stud);

  student.getData();
}
</pre>

<br>

<pre>
class Student {
  final int id;
  final String name;
  final double per;

  Student({required this.id, required this.name, required this.per}) {
    print("Object Created");
  }

  factory Student.fromMap({required Map data}) {
    return Student(
      id: data['id'],
      name: data['name'],
      per: data['per'],
    );
  }

  void getData() {
    print("\nID\t: $id");
    print("NAME\t: $name");
    print("PER\t: $per\n\n");
  }
}

void main() {
  List<Map> studData = [
    {
      'id': 101,
      'name': "Jaynesh Sarkar",
      'per': 89.56,
    },
    {
      'id': 102,
      'name': "Akhil Sarkar",
      'per': 90.4,
    },
    {
      'id': 103,
      'name': "Nayan Thakur",
      'per': 89.56,
    }
  ];

  List<Student> allStudent =
      studData.map((e) => Student.fromMap(data: e)).toList();

  allStudent.forEach((e) {
    e.getData();
  });
}
</pre>

<br><br>

## Inheritance & Its types:

<br>

> * `To Share data from one class to another class.`
> *  To share data among the class.
> *  to exchange data between class.
> *  Here main class which data will be shared is called parent class.
> *  The class which consumes data of another class is called child class.

<br>

### Parent class :
> * `A class whose properties are inherited by another class is called a parent class.`
> * Parent class is also called Super class or Base class.

<br>

### Child class :
> * `A class that itself inherits the properties of another class So such class is called child class.`
> * Child class is also called Sub class or Derived class.


## Types of Inheritance:

<br>

> 1) Simple / Single inheritance
> *  `class 2`
> 2) Multilevel inheritance
> * `min: 3     max: N`
> 3) Hierarchical inheritance
> * `min: 3     max: N    parent: 1   child: N`
> 4) Multiple inheritance
> * `min: 3     max: N    parent: N   child: 1`
> 5) Hybrid inheritance
> * `min: 4     max: N`

<br><br>


### Types of Inheritence in DART:

<br>

> 1) Simple / Single inheritance
> 2) Multilevel inheritance
> 3) Hierarchical inheritance

<br><br>

### NOTE:
> * `Dart does not supports more than 1 Parent class.`
> * `So, the multiple and hybrid inheritance are not possible.`

<br>

## Inheritence in DART:

<br>

> * Extend keyword are used to inherit in Dart.
> * Syntax : `class child_class extends parent_class { }`


<br><br>

### 1) Single level Inheritence :

<br>

> * `In single inheritance, a class can inherit from only one class.`

<br>

> `Minimum class : ` 2 <br>
> `Maximum class : ` 2 <br>

<br>

<p><img src = "https://github.com/SJaynesh/Co-Flutter-ch-06/assets/115562979/8d8c98ce-c9ba-4e7f-8feb-325ed4423bb0.png" width=60% height=50%></p>

<br>


<p><img src = "https://github.com/SJaynesh/Co-Flutter-ch-06/assets/115562979/102c62e7-5b7d-4f9c-9e58-e81e6967950b.png" width=60% height=50%></p>

<br>


<pre>

	class Account

	class User
</pre>

<br>

### 2) Multilevel Inheritence:

<br>

> * `In multilevel inheritance, a class can inherit from a derived class, making the inheritance chain longer.`

<br>

> `Minimum class : ` 3 <br>
> `Maximum class : ` Unlimited <br>

<br>

<p><img src = "https://github.com/SJaynesh/Co-Flutter-ch-06/assets/115562979/6a661c6e-5e39-40bf-90a1-6f3f713a4db2.png" width=60% height=50%></p>

<br>

### 3)  Hierarchical inheritance : 

<br>

> * `Hierarchical inheritance to provide only one Parent class and multiple child class.`
> * Multiple derived classes inherit from a single base class.

<br>

> `Minimum class : ` 3 <br>
> `Maximum class : ` Unlimited <br>


<br>

<p><img src = "https://github.com/SJaynesh/Co-Flutter-ch-06/assets/115562979/410d02b2-595b-4ad4-98ed-c54ac785b2b7.png" width=60% height=50%></p>

<br><br>


## Polymorphism:

<br>

> * Polymorphism is a fundamental concept in object-oriented programming (OOP).
> * `Poly` => Many/Multiple/different
> * `Morphs` => Forms / Structure / behaviour


<br>

> * `It is a concept where any method or attribute have multiple/different behaviours.`

<br>

<p><img src = "https://github.com/SJaynesh/Co-Flutter-ch-06/assets/115562979/1692fb29-3701-42e3-a6ea-74a5021c475a.png" width=60% height=50%></p>

<br>

https://github.com/SJaynesh/CPP-Languge-Ch-08/assets/115562979/d7381d88-6185-4fca-a096-822453572612  
 

<br><br>

## Method Overriding In Dart:

<br>

> * `Create same named method in derived class with same parameters.`
> * When a method in the parent class is redefined within a child class, it is called Method Overriding.

<br>

### Rules:

<br>

> 1) All the methods must have same name.
> 2) All the methods must be in derived(child) class.
> 3) All the method must have same signatures(Parameters, return type).

<br>

<pre>
	
	Class       : Different
	Methid Name : Same 
	Parameters  : Same
	
</pre>

<br>

<pre>
	class Car {
  void showOwner() {
    print("This is parent class car");
  }
}

class Raj extends Car {
  @override
  void showOwner() {
    print("This is Raj class car");
  }
}

void main() {
  Raj raj = Raj();

  raj.showOwner();
}

</pre>

<br><br>

## Exception:

<br>

> * `Logical mistake of code which is unable to handle by compiler`
> * An Exception is runtime object which is occurred in some rare case circumstances(situation).
> * Whenever an exception occur our programs execution flow gets interrupted and halt.
> * Exception is not an error but a one type of situation which compiler cannot handle.
> * An exception causes the program to crash.
> * It Occures by Developer and User both.


<br><br>

## Difference between Error & Exception :

<br>

Error | Exception
-------- | -----------
Syntax mistake of code which is unable to handle by compiler. | Logical mistake of code which is unable to handle by compiler.
It happens on compile time. | It happens on run time.
It Occures by Developer. | It Occures by Developer and User both.


<br><br>


## Exception Handling :

<br>

> * A mechanism by which we can handle anytype of exception is known as exception handling.
> * We can handle any exception using try, on, catch, and finally keyword.

<br><br>

## try Kerword / block :

<br>

> * In this type of block we can write a code that may not leads us towards exception.
> * If any exception occurrs than out flow of execution will be redirected into on block or catch block.

<br><br>

## on block :

<br>

> * We can write as many as on blocks corresponding to different types of exception.
> * We can write such a code in on block that will be executed if and only if an exception is occured from the try block.

<br><br>

## catch block :

<br>

> * The exception raised inside the catch block is handled and its solution is written at the error location of the exception.
> * We can also store the name of the exception that occurs inside the catch block in a variable.
> * Any type of exception raised inside the catch block can be handled. Hence catch block is often called general exception block.

<br><br>

## finally block :

<br>

> * A finally block is a block that will always be executed. That is, whether an exception occurs or not, the coding in the finally block will always be executed.


### Syntax:

<pre>
 	try {
          //code which may cause exception
          //throw [optional since dart provides auto throw of exception class]          
        }
        on [exception-class] {
          //can be used for specific exception only          
        }
        catch(e) {
          //can be use for catch any kind of (general) exceptions.
          //can be used as an exception identifier
        }
        finally {
          //executes each time no matter exception is occured or not.          
        }
</pre>

<br>

### Exception class :

<br>

> * IntegerDivisionByZeroException
> * FormatException
> * UnhandledError
> * MissingPlugginException

<br>

<pre>
import 'dart:io';

void main() {
  int a = 0, b;

  stdout.write("Enter a: ");
  try {
    a = int.parse(stdin.readLineSync()!);
  } on FormatException {
    print("Inbalid format !!");
    return;
    // exit(0);
  }

  stdout.write("Enter b: ");
  b = int.parse(stdin.readLineSync()!);

  try {
    print("Division: ${a ~/ b}");
  } on UnsupportedError {
    print("Cannot devide by ZERO !!");
  } on FormatException {
    print("Invalid format !!");
  } catch (e) {
    print("Exception: $e");
  } finally {
    print("Exception handled successfully !!");
  }
}
</pre>
