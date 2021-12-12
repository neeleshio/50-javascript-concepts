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
12. [Window object]()
13. ['this' keyword]()
14. ['this' context in arrow functions]()
15. [Global space/scope]()
16. [undefined vs not defined vs null]()
17. [Scope chain]()
18. [Lexical scope/environment]()
19. [Lexical 'this']()
20. [let & const]()
21. [var vs let vs const]()
22. [const with objects]()
23. [Temporal dead zone]()
24. [Reference vs Syntax vs Type errors]()
25. [Declaration vs Initialization]()
26. [Arguments vs Parameters]()
27. [Default Parameters]()
28. [Pass by value vs Pass by reference]()
29. [Block scope]()
30. [Shadowing]()
31. [Clousers]()
32. [Uses of Clousers]()
33. [SetTimeout]()
34. [Data hiding using Clousers]()
35. [Disadvantages of Clousers]()
36. [Garbage collectors]()
37. [Types of functions]()
38. [Function statement vs Function expression]()
39. [Named Function expression]()
40. [Function constructors]()
41. [Module design pattern & IIFE]()
42. [First class functions/citizens]()
43. [Pure functions]()
44. [Recurssion]()
45. [Classes]()
46. [Callback functions]()
47. [Main thread blocking]()
48. [Event Listeners]()
49. [Event loop]()
50. [Web APIs]()
51. [Callback Queue]()
52. [Microtask Queue]()
53. [Starvation of callbacks]()
54. [JavaScript Runtime Environment]()
55. [JS Engine]()
56. [Just-in-time compilation]()
57. [Concurrency model]()
58. [Functional Programing]()
59. [DRY]()
60. [Higher order functions]()
61. [Prototype chain]()
62. [Dunder proto]()
63. [Uses of prototype]()
64. [Call, Apply, Bind]()
65. [Promises]()
66. [Async/await]()
67. [Callback hell]()
68. [Imports & dynamic imports]()
69. [Polyfills]()
70. [Currying]()
71. [Coercion]()
72. [Event Bubbling & Event Capturing (trikkling)]()
73. [Event delegation]()
74. [Debouncing & Throtling]()
75. [Objects]()
76. [Rest & spread operators]()
77. [Destructuring]()
78. [Deep copy & shallow copy]()
79. [Array methods & their Big(O)]()
80. [for in vs for of loops]()
81. [map() vs forEach()]()
82. [map() vs reduce() vs filter()]()
83. [Sort vs Numeric sort]()
84. [Map vs Objects vs Sets]()
85. [WeakMap vs WeakSets]()
86. [Memoization]()
87. [Object freeze vs seal vs preventExtension]()
88. [Numeric Seperator]()
89. [DOM APIs]()
90. [Fetch vs Axios]()
91. [Mutation Observer]()
92. [Browser storages]()
93. [Cookies vs Localstorage]()
94. [SessionStorage & CacheStorage]()
95. [Iterators & Generators]()
96. [XSS attack (cross site scripting)]()
97. [CSRF attack]()
98. [ClickJacking]()
99. [CSP (content security policy)]()
100. [Service workers]()


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

## 7. Call stack
A `Call stack` is a data structure where data can be pushed & popped and follows the `LIFO`( Last in First out ) principle.

In JavaScript, the `JavaScript Engine` has its own `Call stack` which keeps track of functions to be executed. So whenever a function is invoked, it is pushed into the `Call stack`.

## 8. Synchronous Single threaded
JavaScript is a `Synchronous Single threaded` language. So when we say `Single threaded` that means it can only execute one command at a time.

So when we say `Synchronous Single threaded` that means it can move to the next command only after it finishes executing the current line/command.

## 9. Hoisting
`Hoisting` is a phenomenon in JS by which we can access variables & functions even before their declaration.

```javascript
console.log(x) // undefined
console.log(foo) // hello from foo

var x = "hello"

function foo() {
  console.log("hello from foo")
}
```

## 10. Arrow functions
`Arrow functions` are an alternative to traditional functions, introduced in `ES6`. Arrow functions are always `Anonymous functions`, so to call them we need to assign it to a variable.

```javascript
const square = a => a * a;

console.log(square(2)) // 4
```

using `Arrow functions`, curly braces, parenthesis, function keyword & return keywords become optional.

## 11. Arrow functions hoisting
