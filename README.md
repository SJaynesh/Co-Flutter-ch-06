# OOP (Object Oriented Programming) 

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
> * `Expression means Single line function.`

<br>

## Function as Expression :
> * `Function as expression means converting a function into short-hand syntax.`
> * Fat-arrow (=>) is used to make any function look like an expression.
> * A function that has a body of only one line, in the function itself expression can be converted. For that { } has to be removed.












