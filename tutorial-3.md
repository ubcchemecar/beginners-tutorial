# Welcome to Tutorial 3: More JavaScript
In Tutorial 2, you used JavaScript to grab, store, manipulate and display data. In this tutorial we will cover more of the basics of JavaScript and compare some of the ideas, syntax and patterns you've learned in APSC 160.

This tutorial is a simplified version of this article, please read it for more information: https://autotelicum.github.io/Smooth-CoffeeScript/literate/js-intro.html#arrays

# 1. Variables

To declare a variable in JavaScript. use `var`. You don't need to declare the data type.

```javascript
var foo = 'hello';      // Declares a string
var num = 1;            // Declares a number
var switch = false;     // Declares a boolean
var array = []          // Declares an empty array
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



# Tutorial 3 - Project
1. Follow our Orgchart tutorial in the Chem-E-Car blog and create a mock orgchart in your website as a separate page (name it orgchart.html or something similar): http://www.ubcchemecar.com/blog/2016/12/24/orgcharts/
2. You can write random names and roles or partially/fully reproduce the Chem-E-Car junior team orgchart, it's up to you.
3. In your main page, index.html, create a link to your orgchart.html page.
