<div align="center">
  <h1>100 Javascript Concepts</h1>
  
  <p><b>JavaScript</b> is a lightweight, Just-in-time compiled, Synchronous Single threaded, Weekly typed programming language.</p>
  
  <img src="https://getflywheel.com/layout/wp-content/uploads/2019/02/The_Best_Java_Script_Libraries_1800x500-1.jpg" alt="JS-banner">
</div>

<br>

## Let's go :)

1. [Data types](#1.-data-types)
2. [var versus let / const](#var-versus-let--const)
3. [ECMAScript & ES6]()
4. [Global Execution Context]()



## Replacing IIFEs with Blocks

> A common use of **Immediately Invoked Function Expressions** is to enclose
values within its scope. In ES6, we now have the ability to create block-based
scopes and therefore are not limited purely to function-based scope.
```javascript
(function () {
    var food = 'Meow Mix';
}());
console.log(food); // Reference Error
```

Using ES6 Blocks:

```javascript
{
    let food = 'Meow Mix';
};
console.log(food); // Reference Error
```

<sup>[(back to table of contents)](#table-of-contents)</sup>

## Arrow Functions

Often times we have nested functions in which we would like to preserve the
context of `this` from its lexical scope. An example is shown below:

```javascript
function Person(name) {
    this.name = name;
}
Person.prototype.prefixName = function (arr) {
    return arr.map(function (character) {
        return this.name + character; // Cannot read property 'name' of undefined
    });
};
```

One common solution to this problem is to store the context of `this` using
a variable:

```javascript
function Person(name) {
    this.name = name;
}
Person.prototype.prefixName = function (arr) {
    var that = this; // Store the context of this
    return arr.map(function (character) {
        return that.name + character;
    });
};
```

We can also pass in the proper context of `this`:

```javascript
function Person(name) {
    this.name = name;
}
Person.prototype.prefixName = function (arr) {
    return arr.map(function (character) {
        return this.name + character;
    }, this);
};
```

As well as bind the context:

```javascript
function Person(name) {
    this.name = name;
}
Person.prototype.prefixName = function (arr) {
    return arr.map(function (character) {
        return this.name + character;
    }.bind(this));
};
```

Using **Arrow Functions**, the lexical value of `this` isn't shadowed and we
can re-write the above as shown:

```javascript
function Person(name) {
    this.name = name;
}
Person.prototype.prefixName = function (arr) {
    return arr.map(character => this.name + character);
};
```

> **Best Practice**: Use **Arrow Functions** whenever you need to preserve the
lexical value of `this`.
Arrow Functions are also more concise when used in function expressions which
simply return a value:

```javascript
var squares = arr.map(function (x) { return x * x }); // Function Expression
```

```javascript
const arr = [1, 2, 3, 4, 5];
const squares = arr.map(x => x * x); // Arrow Function for terser implementation
```

> **Best Practice**: Use **Arrow Functions** in place of function expressions
when possible.
<sup>[(back to table of contents)](#table-of-contents)</sup>

## var versus let / const

> Besides `var`, we now have access to two new identifiers for storing values
—`let` and `const`. Unlike `var`, `let` and `const` statements are not hoisted
to the top of their enclosing scope.
An example of using `var`:

```javascript
var snack = 'Meow Mix';
function getFood(food) {
    if (food) {
        var snack = 'Friskies';
        return snack;
    }
    return snack;
}
getFood(false); // undefined
```

However, observe what happens when we replace `var` using `let`:

```javascript
let snack = 'Meow Mix';
function getFood(food) {
    if (food) {
        let snack = 'Friskies';
        return snack;
    }
    return snack;
}
getFood(false); // 'Meow Mix'
```

This change in behavior highlights that we need to be careful when refactoring
legacy code which uses `var`. Blindly replacing instances of `var` with `let`
may lead to unexpected behavior.

> **Note**: `let` and `const` are block scoped. Therefore, referencing
block-scoped identifiers before they are defined will produce
a `ReferenceError`.
```javascript
console.log(x); // ReferenceError: x is not defined
let x = 'hi';
```

> **Best Practice**: Leave `var` declarations inside of legacy code to denote
that it needs to be carefully refactored. When working on a new codebase, use
`let` for variables that will change their value over time, and `const` for
variables which cannot be reassigned.
<sup>[(back to table of contents)](#table-of-contents)</sup>
