<div align="center">
  <h1>50 Javascript Concepts</h1>
  
  <p><b>JavaScript</b> is a lightweight, Just-in-time compiled, Synchronous Single threaded, Loosly typed programming language.</p>
  
  <img src="https://miro.medium.com/max/3200/1*i8-u-V8LTTbQwTeUwLI_BQ.gif" alt="JS-banner">
</div>

<br>

# Let's go :)

1. [Data types](#1-data-types)
2. [ECMAScript & ES6](#2-ECMAScript-&-ES6)
3. [Most used es6 features](#3-most-used-es6-features)
4. [typeof](#4-typeof)
5. [Execution Context and Global Execution Context](#5-Execution-Context-and-Global-Execution-Context)
6. [2 Phases of code run](#4-2-Phases-of-code-run)
7. [Call stack](#7-Call-stack)
8. [Synchronous Single threaded](#8-Synchronous-Single-threaded)
9. [Hoisting](#9-hoisting)
10. [Arrow functions](#10-arrow-functions)
11. [Arrow functions hoisting](#11-Arrow-functions-hoisting)
12. [Window object](#12-window-object)
13. [Global scope](#13-Global-scope)
14. ['this' keyword](#14-this-keyword)
15. ['this' context in arrow functions](#15-this-context-in-arrow-functions)
16. [Undefined vs not defined vs null](#16-Undefined-vs-not-defined-vs-null)
17. [Scope](#17-Scope)
18. [Types of scope](#18-Types-of-scope)
19. [Lexical scope/environment](#19-lexical-scope)
20. [Scope chain](#20-scope-chain)
21. [Lexical this](#21-lexical-this)
22. [let and const](#22-let-and-const)
23. [var vs let vs const](#23-var-vs-let-vs-const)
24. [const with objects](#24-const-with-objects)
25. [Temporal dead zone](#25-Temporal-dead-zone)
26. [Reference vs Syntax vs Type errors](#26-Reference-vs-Syntax-vs-Type-errors)
27. [Declaration vs Initialization](#27-Declaration-vs-Initialization)
28. [Arguments vs Parameters](#28-Arguments-vs-Parameters)
29. [Default Parameters](#29-Default-Parameters)
30. [Pass by value vs Pass by reference](#30-Pass-by-value-vs-Pass-by-reference)
31. [Block scope](#31-Block-scope)
32. [Shadowing](#32-Shadowing)
33. [Clousers](#33-Clousers)
34. [Uses of Clousers](#34-Uses-of-Clousers)
35. [SetTimeout](#35-SetTimeout)
36. [Data hiding using Clousers](#36-Data-hiding-using-Clousers)
37. [Disadvantages of Clousers](#37-Disadvantages-of-Clousers)
38. [Garbage collectors](#38-Garbage-collectors)
39. [Types of functions](#39-Types-of-functions)
40. [Function statement vs Function expression](#40-Function-statement-vs-Function-expression)
41. [Arguments object](#41-Arguments-object)
42. [Function constructors](#42-Function-constructors)
43. [Module design pattern and IIFE](#43-Module-design-pattern-and-IIFE)
44. [First class functions/citizens](#44-First-class-functions or citizens)
45. [Pure and Impure functions](#45-Pure-and-Impure-functions)
46. [Recurssion](#46-Recurssion)
47. [Classes](#47-Classes)
48. [Callback functions](#48-Callback-functions)
49. [Main thread blocking](#49-Main-thread-blocking)
50. [Event Listeners](#50-Event-Listeners)


**[⬆ Back to Top](#lets-go-)**

## 1. Data types
JavaScript provides 2 types of data-types, `Primitive` type and `Non-Primitive` type.\
<br>
**Primitive type**: Data structure that allows you to store only single data type values.
1. String
2. Number 
3. BigInt
4. Boolean
5. Null
6. Undefined
7. Symbol
<br/>

**NonPrimitive type**: Data structure that allows you to store multiple data type values.
1. Array
2. Object

**[⬆ Back to Top](#lets-go-)**

## 2. JavaScript vs ECMAScript vs ES6
`JavaScript` is a programming language.

`ECMAScript` is the specification for JavaScript.

`ES6` is the most prominent version of JavaScript, released in the year 2015.

**[⬆ Back to Top](#lets-go-)**

## 3. Most used ES6 features.
1. Let & Const
2. Template Literals
3. Arrow Functions
4. Rest & Spread operators
5. Default parameters
6. Destructuring assignment
7. Classes
8. Promises
9. Modules

**[⬆ Back to Top](#lets-go-)**

## 4. typeof
`typeof` operator can be used to find the data type of a value.

```javascript
typeof "superman" // 'string'
typeof "" // 'string'
```
```javascript
typeof 100 // 'number'
```
```javascript
typeof NaN // 'number'
```
```javascript
typeof true // 'boolean'
typeof false // 'boolean'
```
```javascript
typeof 1n // 'bigint'
typeof BigInt(9007199254740991) // 'bigint'
```
```javascript
typeof function(){} // 'function'
```
```javascript
typeof [] // 'object'
```
```javascript
typeof {} // 'object'
```
```javascript
typeof null // 'object'
```
```javascript
typeof new Date() // 'object'
```
```javascript
typeof undefined // 'undefined'
```
```javascript
typeof mycar // 'undefined'
```

**[⬆ Back to Top](#lets-go-)**

## 5. Execution Context & Global Execution Context
Everything in JavaScript happens inside an `Execution context`. An Execution context is like a container or environment where the JavaScript code evaluated & executed.

A `Global execution context` gets created even before it starts to execute any code, so it'll always present at the bottom of the call stack. All the global code i.e. code which is not inside any function or object is executed inside the `Global execution context`. Inside the `Global execution contex`, a new `Execution context` gets created on every time a new function is invoked.

`Execution context` is composed of 2 components,

#### 1. Memory component
This is the place where all the variables and functions are stored as a key-value pairs.

#### 2. Code component
This is where the code gets executed one line at a time.


**[⬆ Back to Top](#lets-go-)**

## 7. Call stack
A `Call stack` is a data structure where data can be pushed & popped and follows the `LIFO`( Last in First out ) principle.

In JavaScript, the `JavaScript Engine` has its own `Call stack` which keeps track of functions to be executed. So whenever a function is invoked, it is pushed into the `Call stack`.


**[⬆ Back to Top](#lets-go-)**

## 8. Synchronous Single threaded
JavaScript is a `Synchronous Single threaded` language. So when we say `Single threaded` that means it can only execute one command at a time.

So when we say `Synchronous Single threaded` that means it can move to the next command only after it finishes executing the current line/command.


**[⬆ Back to Top](#lets-go-)**

## 9. Hoisting
 In plain english `Hoist` means raise or lift. In Javascript `Hoisting` is the default behaviour of moving all the declarations to the top of their scope before code execution. So if we try to access any variables or functions before their declaration, JS won't throw any error. 

In other words, we can also say that `Hoisting` is a phenomenon in JS by which we can access variables & functions even before their declaration.

```javascript
console.log(x) // undefined
console.log(foo()) // hello from foo

var x = "hello"

function foo() {
  console.log("hello from foo")
}
```


**[⬆ Back to Top](#lets-go-)**

## 10. Arrow functions
`Arrow functions` are an alternative to traditional functions, introduced in `ES6`. Arrow functions are always `Anonymous functions`, so to call them we need to assign it to a variable.

```javascript
const square = a => a * a;

console.log(square(2)) // 4
```

using `Arrow functions`, curly braces, parenthesis, function keyword & return keywords become optional.


**[⬆ Back to Top](#lets-go-)**

## 11. Arrow functions hoisting
Like traditional functions, `arrow functions` are not `hoisted` so we can't call them before their declaration.

```javascript
foo() // Uncaught TypeError: foooo is not a function

bar() // Uncaught ReferenceError: fooo is not defined

var foo = () => {
  console.log("hello from foo")
}

const bar = () => {
  console.log("hello from bar")
}
```
Because it behaves just like another variable. It doesn't behave like a function.


**[⬆ Back to Top](#lets-go-)**

## 12. Window object
`Window` is the global object present in the browsers. Every time we run a JS program, the JS engine creates the `window` object.

It consists of lot of useful methods & properties and all the global space variables & functions gets attached to the window object so we can access them anywhere in our program.

```javascript
var a = 10
var b = 20

console.log(window.a) // 10
console.log(window.b) // 20
```

At global level `this` points to `window` object.

```javascript
this === window // true
```

**[⬆ Back to Top](#lets-go-)**

## 13. Global scope
Anything we write inside JS which is not inside the function or block.

```javascript
var x = 10   --> global scoped varibale

function foo () {   --> global scoped function
  var y = 20        --> not global scoped
}
```

**[⬆ Back to Top](#lets-go-)**

## 14. this keyword

1. 'this' keyword refers to the current **object**
2. 'this' keyword always or mostly used in object oriented programming.
3. If we get rid of 'this', we will be left with Javscript as a functional programming language.

The 'this' keyword refers to different objects depending on how it is used:

#### 1. In Method:
In an object method, 'this' refers to the object.

```javascript
const person = {
  fname: 'neelesh',
  lname: 'shetty',
  fullName: function() {
      return this.fname + ' ' + this.lname;  ----> 'this' refers to 'person' object itself.
   }
}

person.fullName() // neelesh shetty
```

#### 2. 'this' alone:
```javascript
let x = this.
console.log(x) // Window {window: Window, self: Window, document: document, name: 'iframeResult', location: Location, …} 
```

when used alone, this refers to `global object`. Becoz 'this' is in global scope.

In a browser window the global object is **[object Window]**.

**In strict mode:**
```javascript
'use strict'
let y = this.
console.log(y) // Window {window: Window, self: Window, document: document, name: 'iframeResult', location: Location, …} 
```

#### 3. In a function:
In a function, it refers to `global object`.

```javascript
function hello() {
  console.log(this)
}

hello() // Window {window: Window, self: Window, document: document, name: 'iframeResult', location: Location, …} 
```

**In strict mode:**
```javascript
'use strict'
function hey() {
  console.log(this)
}

hey() // undefined
```

#### 4. Event handler:
When a function is used as an event handler, its 'this' is set to the element on which the listener is placed.

```javascript
<button onclick="this.style.display='none'">Click to remove button</button>
```

so when we click the button, the above style will get added.


**[⬆ Back to Top](#lets-go-)**

## 15. Arrow function:
An arrow function expression is a compact alternative to a traditional function expression.

### Characteristics:
  1. Using the arrow function, curly braces, paranthesis, function & return keywords become optional.
  2. Arrow functions are always Anonymous functions, so to call arrow function we need to assign it to a variable.
  3. Arrow function expressions should only be used for non-method functions because they do not have their own `this`.
     ```javascript
     const obj = {
        fname: 'neel',
        lname: 'shett',
        getName: () => console.log(this.fname, this) ---> 'this' points to the global window object. 
     }
     
     obj.getName() // undefined, Window {window: Window, self: Window, document: document, name: 'iframeResult', location: Location, …} 
     ```
  4. Arrow functions do not have arguments binding unlike regular functions.
     ```javascript
     const x = () => {
        console.log(arguments);
     }

     x(4,6,7) // ReferenceError: Can't find variable: arguments
     ```
     but with regular function,
     ```javascript
     let x = function () {
        console.log(arguments);
     }
     
     x(4,6,7); // Arguments [4, 6, 7]
     ```
     
     To solve this issue, we can use `spread operator`:
     ```javascript
     let x = (...args) => {
        console.log(args);
     }

     x(4,6,7); // [4, 6, 7]
     ```
  5. Arrow functions provide better syntax to write `promises & callbacks`.
   
     ##### ES5
     ```javascript
     asyncFunction().then(function() {
        return asyncFunction1();
     }).then(function() {
        return asyncFunction2();
     }).then(function() {
        finish;
     });
     ```
     ##### ES6
     ```javascript
     asyncFunction()
      .then(() => asyncFunction1())
      .then(() => asyncFunction2())
      .then(() => finish);
     ```
  6. You cannot use an arrow function as a `constructor`.
     ```javascript
     let Foo = () => {};
     let foo = new Foo(); // TypeError: Foo is not a constructor
     ```
     

## 16. Undefined vs not defined vs null
`undefined` keyword or property indicates that a variable has not been assigned/initialized a value. `undefined` variables takes up their own memory in the memory space.

`not defined` property indicates that a variable is not at all present in the code and in the memory space.

`null` is an object in JavaScript. `null` means nothing & is used to represent an intentional absence of value.


**[⬆ Back to Top](#lets-go-)**

## 17. Scope
`Scope` defines the visibility & availability of variables and functions, meaning it's a place where a defined variable/function can have its existence and beyond that it cannot be accessed.

In JS, we can create `scope` using code blocks, functions & modules.


**[⬆ Back to Top](#lets-go-)**

## 18. Types of scope
There are 3 types of scope in JS:

  #### 1. Global scope
Any variable that is not inside any function or block, is inside the global scope & they are called global scoped variables.

The variables in `global scope` can be accessed from anywhere in the program.

```javascript
var message = "hello"

function printHello() {
  console.log(message)
}

printHello()  // "hello"
```
  #### 2. Function scope
When a variable is declared inside a function, it is only accessible within that function and cannot be used outside that function

`var` is a function scoped, becoz:

```javascript
function hello() {
  if (true) {
    var a = 1;  --- function scoped
    let b = 2;  --- block scoped
    const c = 3; -- block scoped

    console.log(a);
    console.log(b);
    console.log(c);
  }

  console.log(a);
  console.log(b);
  console.log(c);
}

hello();

output: 
1
2
3
1
Reference error: b is not defined.
```
So we can access `var` throughout the function.

  #### 3. Block scope
A variable when declared inside the if or switch conditions or inside for or while loops, are accessible within that particular condition or loop.

As you can see in the above `hello` example, we cannot accesss `b` or `c` outside its if block.


**[⬆ Back to Top](#lets-go-)**

## 19. Lexical scope/environment
Lexical scoping is the environment that holds the variables of the current scope as well as the outer scope.\
or,\
Lexical Environment is the local memory along with the lexical environment of its parent.\
or,\
Lexical scoping is a type of object oriented programming according to which, a child can access parent scope and global scope.


**[⬆ Back to Top](#lets-go-)**

## 20. Scope chain
It is the process in which, JavaScript engine searches for the value of the variables in the scope of the functions. However, the search is in a lexical manner.

First of all the engine looks out in the current scope of the current function. If not found, it finds it in the parent funtion. If not there, global scope is the last place it checks in.\
Hence, to find value of the required variabe, a chain is formed by looking in the different scopes.

```javascript
const a = "Hello world"; -- global scope variable

function first() {
    const b = "I am Neelesh."; -- parent scope variable
    second();

    function second() {
        const c = "A frontend developer"; -- current/local scope variable
        console.log(a + b + c);
    }
}
first();
// Hello world I am Neelesh. A frontend developer
```


**[⬆ Back to Top](#lets-go-)**

## 21. Lexical 'this'
Arrow functions do not have their own value of this. The value of this in an arrow function is inherited from the enclosing (lexical) scope.

It is just a fancy way of saying its value is static and determined by the scope "this" is defined in.

```javascript
const myFunction = () => {
  console.log(this);
};

myFunction() // window
```


**[⬆ Back to Top](#lets-go-)**

## 22. Let & Const
1. Both are introduced in ES6.
2. Variables defined with `let` can be Reassigned.
3. Variables defined with `const` cannot be Reassigned.

### Hoisting
let & const are also hoisted, but very deferently than `var` declaration.

```javascript
console.log(b)  //undefined
console.log(a)  //Reference error: a is not defined

let a = 10
var b = 100
```

Here, `b` gets its memory allocated in the global scope becoz of `var`.
But, `a` gets its memory allocated in the seperate memory space called `Script`. So we can't access let & const before it gets its value.

Note: I tried the above code in different places like,
1. codesandbox.io => output is: // undefined.
2. nodejs => output is: // ReferenceError: Cannot access 'a' before initialization.
3. browser console => output is: // ReferenceError: 'a' is not defined.
4. browser console with index.js => output is: // ReferenceError: Cannot access 'a' before initialization.


**[⬆ Back to Top](#lets-go-)**

## 23. Var vs Let vs Const

|                       var                         |                     let & const                   |
|---------------------------------------------------|---------------------------------------------------|
| 1. var is a function scoped.                      | 1. let & const are block scoped.                  |
| 2. Variables defined with var can be redeclared & | 2. let can be reasigned but cannot be redeclared. |
|    reasigned.                                     |    const cannot be reasigned or redeclared.       |
| 3. It can be accessed without initialization as   | 3. It cannot be accessed without initialization   | 
|    its default value is “undefined”.              |    otherwise it will give ‘referenceError’.       |


**[⬆ Back to Top](#lets-go-)**

## 24. Const with Objects
`Const` allows us to change the Object properties.

```javascript
const obj = { name: 'Bob' }
obj.name = 'silly'

console.log(obj) // { name: 'silly' }
``` 
So, `const` only prevent reassigning of primitive data types.


**[⬆ Back to Top](#lets-go-)**

## 25. Temporal dead zone
The time/period b/w `let` or `const` variable is hoisted & till it initialised some value.

So until it gets some values, the `let` and `const` will be in temporal dead zone. 


**[⬆ Back to Top](#lets-go-)**

## 26. Reference vs Syntax vs Type errors
#### 1. Reference error:
When there is no variable found in the memory.

#### 2. Syntax error:
When there are mistakes in the source code, such as spelling and punctuation errors, incorrect labels, and so on.

#### 3. Type error:
when a value is not of the expected type.

Ex: if a string is attempted to be multiplied with an integer, a `TypeError` is generated.


**[⬆ Back to Top](#lets-go-)**

## 27. Declaration vs Initialisation
`Declaration` declares the creation of variables and functions. or just naming the variable.

`Initialization` occurs when you assign an initial value to a variable.


**[⬆ Back to Top](#lets-go-)**

## 28. Arguments vs Parameters
`Arguments` are the values that are paased to the function during the function call.

`Parameters` are the variables that are used to recieve the arguments that are passed to the function.

```javascript
function printName (name, city) {.  ---- Parameters
  return `Iam {name} from {city}`;
}

printName('Neelesh', 'Ckm') ---- Arguments
```


**[⬆ Back to Top](#lets-go-)**

## 29. Default parameters
`Default parameters` allow named parameters to be initialized with default values if no value or undefined is passed.

```javascript
function multiply(a, b = 1) {  --- 'b' has been initialized with a default value 1. 
  return a * b;
}

console.log(multiply(5, 2));
// Expected output: 10

console.log(multiply(5));
// Expected output: 5
```


**[⬆ Back to Top](#lets-go-)**

## 30. Pass by value vs Pass by reference
When a function is called, the arguments can be passed in two ways, either Pass by value or Pass by reference (address).

**Primitive data** types such as string, number, null, undefined, and boolean, are passed by value while **non-primitive** data types such as objects, arrays, and functions are passed by reference.

`Pass by value` in JavaScript means that a copy of the actual parameter’s value is made in memory. The original value and the copied value are independent of each other as they both have a different space in memory i.e., on changing the value inside the function, the variable outside the function is not affected.

Unlike pass by value, `pass by reference` in does not create a new space in the memory, instead, we pass the reference/address of the actual parameter. Thus, if we change the value of the variable inside the function, then the original value also gets changed.


**[⬆ Back to Top](#lets-go-)**

## 31. Block scope
We use `block` to combine multiple statements.

```javascript
{
        ---- this is a Block.
}
```

Ex: if else statements, for loops etc.


**[⬆ Back to Top](#lets-go-)**

## 32. Shadowing
`shadowing` occurs when a variable declared in a certain scope (e.g. a local variable) has the same name as a variable in an outer scope (e.g. a global variable). When this happens, the outer variable is said to be shadowed by the inner variable.

#### Ex.1: 
```javascript
var a = 100;

{
  var a = 20;
}

console.log(a) // 20
```
First it assigns 100 to `a` & then when it comes at block scoped `a`, it again assigns 20 to the same `a` in the memory. So, value of `a` is 20.

#### Ex.2:
```javascript
let b = 100;

{
  let b = 20;
}

console.log(a) // 100
```
Becoz, `let` is block scoped & shadowing won't happen. Same foe `const`.

Note: It actually creates 2 `b` variables, one in `Global` & another in `Block`.

#### Ex.3:
```javascript
let c = 10;

{
  var c = 20;     ---- illigal shadowing. 
}

console.log(a) // SyntaxError: Identifier 'a' has already been declared
```
#### Ex.4:
```javascript
var a = 100

{
    let a = 20    ---- legal
}

console.log(a) // 100
```


**[⬆ Back to Top](#lets-go-)**

## 33. Clousers
`Closure` is the combination of a function bundled together (enclosed) with references to its surrounding state (the lexical environment).\
or,\
Closure gives you access to an outer function's scope from an inner function.\
or,\
Function along with its lexical scope forms a `closure`.

```javascript
function outer () {
  const a = 7;
  
  function inner () {
    console.log(a)
  }
  
  return inner;
}

const z = outer();
.
...million lines of code
.
z() // 7
```

So, even if we execute the returned function outside its scope, it still remembers its variables with the help of `clousers`.

```javascript
function x() {
  let a = 900;
  
  function y() {
    let b = 7;
    
    function z() {
      console.log(a, b)              Closure:(z)
    }                                   b: 900
    return z;                        Closure:(y)
  }                                     a: 7
  return y;
}

 const a = x()    or just x()()() // 900, 7      
 const b = a()   
 b() // 900, 7
```

Note: Clousers remembers the reference to the variables & not the actual value.


**[⬆ Back to Top](#lets-go-)**

## 34. Uses of Clousers
1. Module design pattern
2. Currying
3. Functions like once
4. memoize
5. Maintaining state in async world
6. SetTimeouts
7. Iterators etc.


**[⬆ Back to Top](#lets-go-)**

## 35. Disadvantages of Clousers
1. Overconsumption of memory becoz variables are not `garbage collected`.
2. If not handled properly then `memory leak` could happen. 


**[⬆ Back to Top](#lets-go-)**

## 36. SetTimeout
JavaScript doesn't wait for none.

```javascript
function x() {
  const a = 1;
  
  setTimeout(() => {
    console.log(a)
  }, [3000])
  
  console.log('hi')
}

x()
//'hi'
// 1
```


**[⬆ Back to Top](#lets-go-)**

## 37. Data hiding using Clousers
Consider this counter function,
```javascript
let count = 0

function counter() {
    counter++
}

counter1()
```
But if we want to prevent any function accessing the `count` variable, we wrap this with another function like below.

```javascript
function counter() {
    let count = 0
    
    return function increment() {
        count++
        return count
    }
}

const counter1 = counter();
counter1()  // 1
counter1()  // 2  
counter1()  // 3  
```
By this method, the variables are safe & also we can create any number of counter instances like counter2 = counter(), this will be a new counter which starts from 0.


**[⬆ Back to Top](#lets-go-)**

## 38. Garbage collectors
If there is any unused variable in the memory, those are `garbage collected`.


**[⬆ Back to Top](#lets-go-)**

## 39. Types of functions
#### 1. Function statement:
A named function is a `Function statement`

```javascript
function a() {
  //.....
}
```

#### 2. Function expression
This is same as function statement but we can omit the function name.

```javascript
const a = function () {
  //....
}
```

#### 3. Anonymous function
Function statement which doesn't have a name or identity.

```javascript
function () {
  //....
}
```

Note: you can't call these type of functions & it gives SynaxError.

#### 4. Named function expression
```javascript
const a = function xyz() {
  console.log('hi')
}
a() // hi
xyz() // ReferenceError: xyz is not defined.
```
So, we can't access xyz outside of that function, becoz it is created as a local scope. Try console logging xyz inside the xyz function itself & you will get the output of the whole xyz function.  

**[⬆ Back to Top](#lets-go-)**

## 40. Function statement vs Function expression
Major difference is `Hoisting`.

```javascript
a() // 'statement'           ---> a: fn{..}
b() // b is not a function ---> b: undefined

function a() {
  console.log('statement')
}

const b = function() {
  console.log('expression')
}
```
So, function statements are hoisted as a variables.

**[⬆ Back to Top](#lets-go-)**

## 41. Arguments object
The arguments of a function are maintained in an array-like object. Within a function, you can address the arguments passed to it as follows:
```javascript
arguments[i];
```
```javascript
function myConcat(separator) {
  let result = ""; // initialize list
  // iterate through arguments
  for (let i = 1; i < arguments.length; i++) {
    result += arguments[i] + separator;
  }
  return result;
}

myConcat("; ", "elephant", "giraffe", "lion", "cheetah") // "elephant; giraffe; lion; cheetah; "
```


## 42. Function constructors
The Function() constructor creates a new Function object. Calling the constructor directly can create functions dynamically, but suffers from security and similar (but far less significant) performance issues as eval() becoz we are trying to evaluate string as Javascript.

Function constructor creates functions which execute in the global scope only.

```javascript
const sum = new Function('a', 'b', 'return a + b');

sum(2, 6) // 8
```
Note: Function() can be called with or without new. Both create a new Function instance.

Warning: This type of methods are not recommended.

**[⬆ Back to Top](#lets-go-)**

## 43. Module design pattern and IIFE
The module pattern is a design pattern used for improving the maintainability and reusability of the code by creating `public` and `private` access levels.

Sometimes called `encapsulation`, it protects the value inside a module from being accessed from other scopes.

**[⬆ Back to Top](#lets-go-)**

## 44. First class functions or citizens
A programming language is said to have `First-class` functions when functions in that language are treated like any other variable. 

For example, in such a language, a function can be passed as an argument to other functions, can be returned by another function and can be assigned as a value to a variable.

#### Assigning a function to a variable:
```javascript
const foo = () => {
  console.log("foobar");
};
foo(); // Invoke it using the variable
```

#### Passing a function as an argument:
```javascript
function greeting(helloMessage, name) {
  console.log(helloMessage() + name);
}
function sayHello() {
  return "Hello, ";
}
// Pass `sayHello` as an argument to `greeting` function
greeting(sayHello, "JavaScript!");
// Hello, JavaScript!
```

#### Returning a function:
```javascript
function sayHello() {
  return () => {
    console.log("Hello!");
  };
}
```

**[⬆ Back to Top](#lets-go-)**

## 45. Pure and Impure functions
A pure function is a function that returns the same result if the same arguments(input) are passed to the function.

1. The return value of the function on the function call should only be dependent on the input function arguments.

2. It should not modify any non-local state. It means the function should not manipulate anything other than the data stored in the local variables declared within the function.

```javascript
function operationAdd(a, b){ // A pure function adding two integers passed in it.
    return a+b;
}

function operationDivide(a, b){  // Pure function to divide two integers passed in it.
    return a/b;
}

function operationMulti(a, b){    // Pure function to multiple two integers passed in it.
    return a*b;
}
console.log(        // Calling all the pure functions
  operationAdd(2,5),
  operationMulti(3,2),
  operationDivide(20,5)
);
```

#### Why Use Pure Functions?

1. Better Readability:
Pure functions increase the readability of the javascript code because of its simplicity.

2. Testable:
It's easier to perform unit testing on a pure function than on an impure function. A pure function result only depends upon its input arguments hence the whole function can be treated as an independent entity. So we can just take that function and test it with some standard input values whose output is known.

3. Better Performance:
Pure functions can be memoized and this makes your application faster.

### Impure function
An impure function gives inconsistent results or different results for the same input values.

```javascript
 function impureFunc(myArray, item) {
     return myArray.push(item);
 }
```
In the above example, we are manipulating the myArray argument and a pure function should not change(manipulate) any part of the code. That's why this is an impure function.

#### Returning value dependent on the non-local state:
```javascript
const message = 'Hi there! ';
 function myMessage(value) {
     return `${message} ${value}`
 }
 console.log(myMessage('hello'));
```
In the above code, the result the function is returning is dependent on the variable that is not declared inside the function, that's why this is an impure function.

#### Some side effects:
1. Making an HTTP request
2. Mutating data
3. Printing to a screen or console
4. DOM Query/Manipulation
5. Using Math.random()
6. Getting the current time

**[⬆ Back to Top](#lets-go-)**

## 46. Recurssion
Recursion is a process of calling itself. A function that calls itself is called a recursive function.

#### Characteristics:
1. A recursive function must have a condition to stop calling itself. Otherwise, the function is called `indefinitely`.
2. Once the condition is met, the function stops calling itself. This is called a `base condition`.

```javascript
// program to find the factorial of a number
function factorial(x) {
    if (x < 0) return 'Invalid input'
    if (x === 0) {
        return 1;
    } else {
        return x * factorial(x - 1);
    }
}
factorial(3) // 6
```

**[⬆ Back to Top](#lets-go-)**

## 47. Classes
Classes are a template for creating objects.

#### Characteristics:
1. Classes were introduced in `EcmaScript 2015 (ES6)` to provide a cleaner way to follow object-oriented programming patterns.
2. JavaScript still follows a prototype-based inheritance model. Classes in JavaScript are syntactic sugar over the prototype-based inheritance model which we use to implement OOP concepts.
3. Thus the introduction of classes in JS made it easier for developers to build software around OOP concepts. It also brought in similarities to different OOP-based programming languages such as C++ and Java.
4. Before classes, we used constructor functions to do OOP in JavaScript. Have a look at the example below:

```javascript
function Pen(name, color, price) {
    this.name = name;
    this.color = color;
    this.price = price;
}

const pen1 = new Pen("Marker", "Blue", "$3");

// Adding function in a constructor
Pen.prototype.showPrice = function(){
    console.log(`Price of ${this.name} is ${this.price}`);
}

pen1.showPrice();
```

We can re-create the above example much cleaner with the help of the Class keyword:
```javascript
class Pen {
    constructor(name, color, price){
        this.name = name;
        this.color = color; 
        this.price = price;
    }
    
    showPrice(){
        console.log(`Price of ${this.name} is ${this.price}`);
    }
}

const pen1 = new Pen("Marker", "Blue", "$3");
pen1.showPrice();
```

**[⬆ Back to Top](#lets-go-)**

## 48. Callback functions
A callback function is a function passed into another function as an argument.

The benefit of using a callback function is that we can wait for the result of a previous function call and then execute another function call.
```javascript
function greeting(name) {.  --> callback function
  alert(`Hello, ${name}`);
}

function processUserInput(cb) {
  const name = prompt("Please enter your name.");
  cb(name);
}

processUserInput(greeting);
```
The above example is a `synchronous` callback, as it is executed immediately.

However, callbacks are often used to continue code execution after an `asynchronous` operation has completed.
A good example is the callback functions executed inside a `.then()` block chained onto the end of a promise after that promise fulfills or rejects.

**[⬆ Back to Top](#lets-go-)**

## 49. Main thread blocking
The browser uses a single thread to run all the JavaScript in your page, as well as to perform layout, reflows, and garbage collection.

This means that long-running JavaScript functions can block the thread, leading to an unresponsive page and a bad user experience.

For example: An image transformation which needs 10sec to be computed, you are blocking the UI responses (ex. JS animations, clicks, inputs, typing, etc.)

So the browser itself could decide to take action and show a popup to the user asking whether to `kill that process` or keep it running.

#### Workarounds to this problem: (So we can run a long script as well as not blocking our UI)
1. Create a WebWorker:
It is an API for running JavaScript code in a different browser’s thread. Its limitation is it has no access to the DOM. It can communicate with the main thread only via messages.

It is useful for running your computation outside the main thread and once finished getting the response for it. Though if your code needs frequent access to read and manipulate the DOM, maybe this is not the best option.

2. Slice your long-task in little sub-tasks and run them asynchronously:
We can use the setTimeout API for this and take advantage of the Event queue logic to have other things (Job queue and Rendering).

**[⬆ Back to Top](#lets-go-)**

## 50. Event Listeners
An event listener is a function that runs once a specific event occurs. So, an event listener “listens” for an action, then calls a function that performs a related task.

You can listen for events on any element in the DOM. JavaScript has an addEventListener() function that you can call on any element on a web page.

```javascript
document.querySelector('.btn').addEventListener("click", clickDemo)

function clickDemo(){
    console.log("Hi there")
}
```
`Event-driven programming` is the name of a paradigm that relies on the execution of an event to perform its functions.

**[⬆ Back to Top](#lets-go-)**
