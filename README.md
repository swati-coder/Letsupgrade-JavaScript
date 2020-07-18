# Letsupgrade-JavaScript Day 1 Assignment

Q.1
Methods of console function:
1.console.log() method 

console.log('abc');  
console.log(1); 

console.log(true); 

console.log(null); 
console.log(undefined);  

console.log([1, 2, 3, 4]); 

console.log({a:1, b:2, c:3}); 

Output:
abc
1
true 
null
undefined
Array(4) [1,2,3,4]
Object {a: 1,b: 2,c: 3}
>>
2.console error method

console.error('This is a simple error');  
Output:
This is a simple error

3.console warn method
console.warn('This is a warning.'); 
Output:
This is a warning

4.console clear
console.clear();
Output:
Screen cleared

5.console.time() 
6.console.timeEnd() method  

console.time('abc'); 

 let fun =  function(){ 

     console.log('fun is running'); 

 } 

 let fun2 = function(){ 

     console.log('fun2 is running..'); 

 } 

 fun(); // calling fun(); 

 fun2(); // calling fun2(); 

console.timeEnd('abc'); 
Output:
fun is running
fun2 is running..
abc:1ms
>>
7.console.table() method 

console.table({'a':1, 'b':2}); 
Output:
console.table()
(index)
a
b
>>

8.console.count() method 

for(let i=0;i<5;i++){ 

    console.count(i); 
} 
Output:
0: 1
1: 1
2: 1
3: 1
4: 1
 
9.console.group() 
10. console.groupEnd() method 

console.group('simple'); 
  console.warn('warning!'); 
  console.error('error here'); 
  console.log('vivi vini vici'); 
console.groupEnd('simple'); 
console.log('new section');
output:
simple
  warning!
  error here
  vivi vini vici
new section
 

11.Custom Console log example 
  const spacing = '10px'; 
  const styles =  
        `padding: ${spacing}; background-color: white; color: green; font-style:  
         italic; border: 1px solid black; font-size: 2em;`; 
  console.log('%c I Love JavaScript', styles); 
  output:
  I Love JavaScript
  
  Q.2 Difference between var, let, const
a) Var:
The JavaScript variables statement is used to declare a variable and, optionally, we can initialize the value of that variable.

Example: var a =10;

Variable declarations are processed before the execution of the code.
The scope of a JavaScript variable declared with var is its current execution context.
The scope of a JavaScript variable declared outside the function is global.
Consider the following code snippet.

function nodeSimplified(){
  var a =10;
  console.log(a);  // output 10
  if(true){
   var a=20;
   console.log(a); // output 20
  }
  console.log(a);  // output 20
}
In the above code, you can find, when the variable is updated inside the if loop, that the value of variable "a" updated 20 globally, hence outside the if loop the value persists. It is similar to the Global variable present in other languages. But, be sure to use this functionality with great care because there is the possibility of overriding an existing value.

b)let:
The let statement declares a local variable in a block scope. It is similar to var, in that we can optionally initialize the variable.

Example: let a =10;

The let statement allows you to create a variable with the scope limited to the block on which it is used.
It is similar to the variable we declare in other languages like Java, .NET, etc.
Consider the following code snippet.

function nodeSimplified(){
  let a =10;
  console.log(a);  // output 10
  if(true){
   let a=20;
   console.log(a); // output 20
  }
  console.log(a);  // output 10
}
It is almost the same behavior we see in most language.

function nodeSimplified(){
  let a =10;
  let a =20; //throws syntax error
  console.log(a); 
}
Error Message: Uncaught SyntaxError: Identifier 'a' has already been declared.

However, with var, it works fine.

function nodeSimplified(){ 
  var a =10;   
  var a =20;   
  console.log(a);  //output 20 
}
The scope will be well maintained with a let statement and when using an inner function the let statement makes your code clean and clear.

I hope the above examples will help you better understand the var and let commands and if you have any queries please write me in the comment section.

c) const
const statement values can be assigned once and they cannot be reassigned. The scope of const statement works similar to let statements.

Example: const a =10;

function nodeSimplified(){
  const MY_VARIABLE =10;
  console.log(MY_VARIABLE);  //output 10 
}
As per usual, naming standards dictated that we declare the const variable in capital letters. const a =10 will work the same way as the code given above. Naming standards should be followed to maintain the code for the long run.
  
Q.3 Data Types of JavaScript
1.The String Data Type
The string data type is used to represent textual data (i.e. sequences of characters). Strings are created using single or double quotes surrounding one or more characters, as shown below:

Example
var a = 'Hi there!';  // using single quotes
var b = "Hi there!";  // using double quotes
You can include quotes inside the string as long as they don't match the enclosing quotes.

Example
var a = "Let's have a cup of coffee."; // single quote inside double quotes
var b = 'He said "Hello" and left.';  // double quotes inside single quotes
var c = 'We\'ll never give up.';     // escaping single quote with backslash

2.The Number Data Type
The number data type is used to represent positive or negative numbers with or without decimal place, or numbers written using exponential notation e.g. 1.5e-4 (equivalent to 1.5x10-4).

Example
var a = 25;         // integer
var b = 80.5;       // floating-point number
var c = 4.25e+6;    // exponential notation, same as 4.25e6 or 4250000
var d = 4.25e-6;    // exponential notation, same as 0.00000425
The Number data type also includes some special values which are: Infinity, -Infinity and NaN. Infinity represents the mathematical Infinity ∞, which is greater than any number. Infinity is the result of dividing a nonzero number by 0, as demonstrated below:

Example
alert(16 / 0);  // Output: Infinity
alert(-16 / 0); // Output: -Infinity
alert(16 / -0); // Output: -Infinity
While NaN represents a special Not-a-Number value. It is a result of an invalid or an undefined mathematical operation, like taking the square root of -1 or dividing 0 by 0, etc.

Example
alert("Some text" / 2);       // Output: NaN
alert("Some text" / 2 + 10);  // Output: NaN
alert(Math.sqrt(-1));         // Output: NaN

3.The Boolean Data Type
The Boolean data type can hold only two values: true or false. It is typically used to store values like yes (true) or no (false), on (true) or off (false), etc. as demonstrated below:

Example
var isReading = true;   // yes, I'm reading
var isSleeping = false; // no, I'm not sleeping
Boolean values also come as a result of comparisons in a program. The following example compares two variables and shows the result in an alert dialog box:

Example
var a = 2, b = 5, c = 10;
 
alert(b > a) // Output: true
alert(b > c) // Output: false

4.The Boolean Data Type
The Boolean data type can hold only two values: true or false. It is typically used to store values like yes (true) or no (false), on (true) or off (false), etc. as demonstrated below:

Example
var isReading = true;   // yes, I'm reading
var isSleeping = false; // no, I'm not sleeping
Boolean values also come as a result of comparisons in a program. The following example compares two variables and shows the result in an alert dialog box:

Example
var a = 2, b = 5, c = 10;
 
alert(b > a) // Output: true
alert(b > c) // Output: false

5.The Null Data Type
This is another special data type that can have only one value-the null value. A null value means that there is no value. It is not equivalent to an empty string ("") or 0, it is simply nothing.

A variable can be explicitly emptied of its current contents by assigning it the null value.

Example
var a = null;
alert(a); // Output: null
 
var b = "Hello World!"
alert(b); // Output: Hello World!
 
b = null;
alert(b) // Output: null

6.The Object Data Type
The object is a complex data type that allows you to store collections of data.

An object contains properties, defined as a key-value pair. A property key (name) is always a string, but the value can be any data type, like strings, numbers, booleans, or complex data types like arrays, function and other objects. You'll learn more about objects in upcoming chapters.

The following example will show you the simplest way to create an object in JavaScript.

Example
var emptyObject = {};
var person = {"name": "Clark", "surname": "Kent", "age": "36"};
 
// For better reading
var car = {
    "modal": "BMW X3",
    "color": "white",
    "doors": 5
}
You can omit the quotes around property name if the name is a valid JavaScript name. That means quotes are required around "first-name" but are optional around firstname. So the car object in the above example can also be written as:

Example
var car = {
    modal: "BMW X3",
    color: "white",
    doors: 5
}

7.The Array Data Type
An array is a type of object used for storing multiple values in single variable. Each value (also called an element) in an array has a numeric position, known as its index, and it may contain data of any data type-numbers, strings, booleans, functions, objects, and even other arrays. The array index starts from 0, so that the first array element is arr[0] not arr[1].

The simplest way to create an array is by specifying the array elements as a comma-separated list enclosed by square brackets, as shown in the example below:

Example
var colors = ["Red", "Yellow", "Green", "Orange"];
var cities = ["London", "Paris", "New York"];
 
alert(colors[0]);   // Output: Red
alert(cities[2]);   // Output: New York

8.The Function Data Type
The function is callable object that executes a block of code. Since functions are objects, so it is possible to assign them to variables, as shown in the example below:

Example
var greeting = function(){ 
    return "Hello World!"; 
}
 
// Check the type of greeting variable
alert(typeof greeting) // Output: function
alert(greeting());     // Output: Hello World!
In fact, functions can be used at any place any other value can be used. Functions can be stored in variables, objects, and arrays. Functions can be passed as arguments to other functions, and functions can be returned from functions. Consider the following function:

Example
function createGreeting(name){
    return "Hello, " + name;
}
function displayGreeting(greetingFunction, userName){
    return greetingFunction(userName);
}
 
var result = displayGreeting(createGreeting, "Peter");
alert(result); // Output: Hello, Peter
