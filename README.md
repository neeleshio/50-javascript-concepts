<div align="center">
  <h1>100 Javascript Concepts</h1>
  
  <p><b>JavaScript</b> is a lightweight, Just-in-time compiled, Synchronous Single threaded, Weekly typed programming language.</p>
  
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
13. [Global space/scope]()
14. ['this' keyword]()
15. ['this' context in arrow functions]()
16. [undefined vs not defined vs null]()
17. [Scope]()
18. [Types of scope]()
19. [Lexical scope/environment]()
20. [Scope chain]()
21. [Lexical 'this']()
22. [let & const]()
23. [var vs let vs const]()
24. [const with objects]()
25. [Temporal dead zone]()
26. [Reference vs Syntax vs Type errors]()
27. [Declaration vs Initialization]()
28. [Arguments vs Parameters]()
29. [Default Parameters]()
30. [Pass by value vs Pass by reference]()
31. [Block scope]()
32. [Shadowing]()
33. [Clousers]()
34. [Uses of Clousers]()
35. [SetTimeout]()
36. [Data hiding using Clousers]()
37. [Disadvantages of Clousers]()
38. [Garbage collectors]()
39. [Types of functions]()
40. [Function statement vs Function expression]()
41. [Named Function expression]()
42. [Function constructors]()
43. [Module design pattern & IIFE]()
44. [First class functions/citizens]()
45. [Pure functions]()
46. [Recurssion]()
47. [Classes]()
48. [Callback functions]()
49. [Main thread blocking]()
50. [Event Listeners]()
51. [Event loop]()
52. [Web APIs]()
53. [Callback Queue]()
54. [Microtask Queue]()
55. [Starvation of callbacks]()
56. [JavaScript Runtime Environment]()
57. [JS Engine]()
58. [Just-in-time compilation]()
59. [Concurrency model]()
60. [Functional Programing]()
61. [DRY]()
62. [Higher order functions]()
63. [Prototype chain]()
64. [Dunder proto]()
65. [Uses of prototype]()
66. [Call, Apply, Bind]()
67. [Promises]()
68. [Async/await]()
69. [Callback hell]()
70. [Imports & dynamic imports]()
71. [Polyfills]()
72. [Currying]()
73. [Coercion]()
74. [Event Bubbling & Event Capturing (trikkling)]()
75. [Event delegation]()
76. [Debouncing & Throtling]()
77. [Objects]()
78. [Rest & spread operators]()
79. [Destructuring]()
80. [Deep copy & shallow copy]()
81. [Array methods & their Big(O)]()
82. [for in vs for of loops]()
83. [map() vs forEach()]()
84. [map() vs reduce() vs filter()]()
85. [Sort vs Numeric sort]()
86. [Map vs Objects vs Sets]()
87. [WeakMap vs WeakSets]()
88. [Memoization]()
89. [Object freeze vs seal vs preventExtension]()
90. [Numeric Seperator]()
91. [DOM APIs]()
92. [Fetch vs Axios]()
93. [Mutation Observer]()
94. [Browser storages]()
95. [Cookies vs Localstorage]()
96. [SessionStorage & CacheStorage]()
97. [Iterators & Generators]()
98. [XSS attack (cross site scripting)]()
99. [CSRF attack]()
100. [ClickJacking]()
101. [CSP (content security policy)]()
102. [Service workers]()


**[⬆ Back to Top](#lets-go-)**





## 1. Data types
JavaScript provides 2 types of data-types, `Primitive` type and `Non-Primitive` type.
#### Primitive type:
1. String
2. Number 
3. BigInt
4. Boolean
5. Null
6. Undefined
7. Symbol
#### Non-Primitive type:
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

## 13. Global space/scope
Anything we write inside JS which is not inside the function or block.

```javascript
var x = 10   --> global scoped varibale

function foo () {   --> global scoped function
  var y = 20        --> not global scoped
}
```


**[⬆ Back to Top](#lets-go-)**

## 16. undefined vs not defined vs null
`undefined` keyword or property indicates that a variable has not been assigned/initialized a value. `undefined` variables takes up their own memory in the memory space.

`not defined` property indicates that a variable is not at all present in the code and in the memory space.

`null` is an object in JavaScript. `null` means nothing & is used to represent an intentional absence of value.


**[⬆ Back to Top](#lets-go-)**

## 17. Scope
`Scope` defines the visibility & availability of variables and functions, meaning it's a place where a defined variable/function can have its existence and beyond that it cannot be accessed.

In JS, we can create `scope` using code blocks, functions & modules.

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
#### 2. Local or Function scope
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

## 19. Lexical scope/environment
Lexical scoping is the environment that holds the variables of the current scope as well as the outer scope.
or
Lexical Environment is the local memory along with the lexical environment of its parent.
or
Lexical scoping is a type of object oriented programming according to which, a child can access parent scope and global scope

## 20. Scope chain
It is the process in which, JavaScript engine searches for the value of the variables in the scope of the functions. However, the search is in a lexical manner.

First of all the engine looks out in the current scope of the current function. If not found, it finds it in the parent funtion. If not there, global scope is the last place it checks in.
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
## 21. Lexical 'this'
<--- loading --->

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

## 23. Var vs Let vs Const

|                       var                         |                     let & const                   |
|---------------------------------------------------|---------------------------------------------------|
| 1. var is a function scoped.                      | 1. let & const are block scoped.                  |
| 2. Variables defined with var can be redeclared & | 2. let can be reasigned but cannot be redeclared. |
|    reasigned.                                     |    const cannot be reasigned or redeclared.       |
| 3. It can be accessed without initialization as   | 3. It cannot be accessed without initialization   | 
|    its default value is “undefined”.              |    otherwise it will give ‘referenceError’.       |

## 24. Const with Objects
`Const` allows us to change the Object properties.

```javascript
const obj = { name: 'Bob' }
obj.name = 'silly'

console.log(obj) // { name: 'silly' }
``` 
So, `const` only prevent reassigning of primitive data types.

## 25. Temporal dead zone
The time/period b/w `let` or `const` variable is hoisted & till it initialised some value.

So until it gets some values, the `let` and `const` will be in temporal dead zone. 

## 26. Reference vs Syntax vs Type errors
#### 1. Reference error:
When there is no variable found in the memory.

#### 2. Syntax error:
When there are mistakes in the source code, such as spelling and punctuation errors, incorrect labels, and so on.

#### 3. Type error:
when a value is not of the expected type.

Ex: if a string is attempted to be multiplied with an integer, a `TypeError` is generated.

## 27. Declaration vs Initialisation
`Declaration` declares the creation of variables and functions. or just naming the variable.

`Initialization` occurs when you assign an initial value to a variable.

## 28. Arguments vs Parameters
`Arguments` are the values that are paased to the function during the function call.

`Parameters` are the variables that are used to recieve the arguments that are passed to the function.

```javascript
function printName (name, city) {.  ---- Parameters
  return `Iam {name} from {city}`;
}

printName('Neelesh', 'Ckm') ---- Arguments
```

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

## 30. Pass by value vs Pass by reference
<--- loading --->

## 31. Block scope
We use `block` to combine multiple statements.

```javascript
{
        ---- this is a Block.
}
```

Ex: if else statements, for loops etc.

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

## 33. Clousers
`Closure` is the combination of a function bundled together (enclosed) with references to its surrounding state (the lexical environment). 
or,
Closure gives you access to an outer function's scope from an inner function.
or,
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

## 34. Uses of Clousers
1. Module design pattern
2. Currying
3. Functions like once
4. memoize
5. Maintaining state in async world
6. SetTimeouts
7. Iterators etc.

## 35. Disadvantages of Clousers
1. Overconsumption of memory becoz variables are not `garbage collected`.
2. If not handled properly then `memory leak` could happen. 

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

## 38. Garbage collectors
If there is any unused variablein the memory, those are `garbage collected`.

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
So, we can't access xyz outside of that function, becoz it is created as a local scope. Try console logging xyz inside the xyz function itseld & it will outside whole xyz function.  
