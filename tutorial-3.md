# Welcome to Tutorial 3: More JavaScript
In Tutorial 2, you used JavaScript to grab, store, manipulate and display data. In this tutorial we will cover more of the basics of JavaScript and compare some of the ideas, syntax and patterns you've learned in APSC 160.

This tutorial is a simplified version of this article, please read it for more information: [JavaScript Basics](https://autotelicum.github.io/Smooth-CoffeeScript/literate/js-intro.html)

# 1. Variables

To declare a variable in JavaScript. use `var`. You don't need to declare the data type.

```javascript
var foo = 'hello';      // Declares a string
var num = 1;            // Declares a number
var array = [];          // Declares an empty array
var object = {};        // Declares an empty object
```

# 2. Arrays
### Declaring Arrays
Unlike C, arrays in JavaScript can have elements of different data types:

```javascript
var weekDays = ['Mon', 'Tues', 'Wed', 'Thurs'];       // Array of strings
var myArray = [1, 'Tues', 'Wed', true];            // Arrays of numbers, strings and booleans
```

### Accessing Arrays

Arrays are zero-indexed, the first element of the array is at index 0. For example, weekDays[0] will return 'Mon':
```javascript
var weekDays = ['Mon', 'Tues', 'Wed', 'Thurs'];       // Array of strings
var today = weekDays[0] // stores 'Mon' in today
```

### Array Manipulation
There are several array methods available for manipulating arrays, `pop()`, `push()`, `shift()` and `splice()`. Read this article to find out more: http://www.w3schools.com/js/js_array_methods.asp

# 3. Functions
Functions can be declared in different ways. The following are equivalent ways of declaring a function called `foo`:

```javascript
function foo() { /* do something */ }
var foo = function() { /* do something */ }
```

You can also define parameters in your function:

```javascript
function functionName(parameter1, parameter2, parameter3) {
    // code to be executed
}
```

Once you've defined your function, you can call it:

```javascript
function addNumbers(x, y){
  return (x+y);
}

var number = addNumbers(1,2) // returns 3
```

# 4. Scopes
In JavaScript, scope is the set of variables, objects, and functions you have access to.

### Variables declared outside functions
A variable declared outside a function, becomes GLOBAL. A global variable has global scope: All scripts and functions on a web page can access it. 

```javascript
var carName = " Volvo";

// code here can use carName

function myFunction() {

    // code here can use carName 

}
```

### Variables declared inside functions
Variables declared inside a function are local to that function. Local variables have local scope: They can only be accessed within the function.

```javascript
// code here can not use carName

function myFunction() {
    var carName = "Volvo";

    // code here can use carName

}
```

However, if you assign a value to a variable that has not been declared, it will automatically become global even if it is inside a function:

```javascript
myFunction();

// code here can use carName 

function myFunction() {
    carName = "Volvo";
}
```

Further reading: http://www.w3schools.com/js/js_scope.asp

# 5. Objects
We talked about objects in Tutorial 2, and here's a short refresher.

You can declare an empty object as follows:

```javascript
var ChemECar = {};
```

Properties of an object are stored as key-value pairs, for example, this defines a ChemECar object with 2 keys, battery, year, and 2 corresponding values, a "Zinc-Air" string and a 2017 number:

```javascript
var ChemECar = {
    battery:"Zinc-Air",
    year: 2017
};
```

Further reading: 

1. http://www.w3schools.com/js/js_object_definition.asp 
2. http://javascript.info/tutorial/objects

# 6. Callbacks
Unlike C in APSC160, functions in JavaScript are also objects. That means we can actually pass around functions as arguments to another function. 

Read this article: [JavaScript Callbacks Explained Using Minions](https://medium.freecodecamp.com/javascript-callbacks-explained-using-minions-da272f4d9bcd#.79amnvwvb)

# 7. More Coming Soon
This tutorial is currently a work in progress, please try the orgchart project below.

# Tutorial 3 - Project
1. Follow our Orgchart tutorial in the Chem-E-Car blog and create a mock orgchart in your website as a separate page (name it orgchart.html or something similar): http://www.ubcchemecar.com/blog/2016/12/24/orgcharts/
2. You can write random names and roles or partially/fully reproduce the Chem-E-Car junior team orgchart, it's up to you.
3. In your main page, index.html, create a link to your orgchart.html page.
4. Play around with the styles and fonts of the orgchart using CSS.

