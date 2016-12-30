# Welcome to Tutorial 2 - JavaScript (JS)
So far, you've worked on raw, static HTML in Tutorial 1 but in Tutorial 1.3, you may have noticed some JavaScript `.js` files in the Bootstrap framework. If you've used some dynamic Bootstrap components like dropdown menus in Tutorial 1.3, you've (perhaps unknowingly) used JavaScript.

Essentially, HTML is a markup language designed for defining static web page content. JavaScript is a programming language designed for performing dynamic tasks.

> JavaScript: Love it or hate it, it’s a popular programming language for many, mainly because it’s so incredibly easy to learn. And if you’re a web developer, it’s almost a requirement of the job to have a working knowledge of JavaScript.

Read this article to find out why JavaScript is important: https://blog.jscrambler.com/javascript-the-perfect-language-for-the-internet-of-things-iot/

### Intro to Javascript
In Tutorial 1, we used HTML to design a static website. In this tutorial, we will learn how to make our website more interactive by using JavaScript to retrieve, manipulate and display data.

Specifically, we will be examining the process of getting data from another webserver (specifically, a [REST API](https://www.youtube.com/watch?v=7YcW25PHnAA)) and displaying the data your own webpage with the help of the `jQuery` library. `jQuery` is a JavaScript library that helps us write JavaScript code easier and faster using a simpler syntax. 

Before you begin, 

- [Read this article](http://www.htmlgoodies.com/tutorials/forms/article.php/3895776/HTML-Forms-jQuery-Basics---Getting-Started.htm) for further information on jQuery. 

- [And also this article on jQuery](https://learn.jquery.com/about-jquery/how-jquery-works/)

# 0. Inspect the Data
Our goal is to grab data from our Molson API: http://molson.ubcchemecar.com/api and display it on our website. Before you continue, please read this short 3-minute article and understand the concept of an API: http://sproutsocial.com/insights/what-is-an-api/

Open the Molson API link in your browser, and you should see something like this:

```javascript
{ "timestamp":"2016-12-28T01:47:59.970Z",
  "data":
    { "temperature":11,
      "pH":7 }
}
```
The data from the Molson API is the time, temperature and pH in JSON (JavaScript Object Notation) format. JSON is essentially text (human-readable), but in a special format such that it can be easily converted into JavaScript objects. 

- [Read this article](https://www.copterlabs.com/json-what-it-is-how-it-works-how-to-use-it/) on JSON to find out why it matters

## JavaScript Objects
Recall your intro to programming lessons from first year engineering. In APSC 160, you can define variables as different data types in C, for example, integers, characters and floats:

```C
int myInteger = 1;
char myCharacter = 'c';
float myNumber = 3.14;
```

We can declare our variables in a similar manner in JavaScript, but we do not need to define the type of the variables:
```javascript
var myInteger = 1;
var myCharacter = 'c';
var myNumber = 3.14;
```

JavaScript is an object-oriented language. Almost 'everything' in Javascript is an object. Objects are (essentially) variables containing variables.

As an example, here's a Chem-E-Car variable, which is an Object:

```javascript
var ChemECar = new Object(); // this is the same as var ChemECar = {};
```
We can store new properties in the ChemECar variable as key-value pairs:
```javascript
ChemECar = {
    battery:"Zinc-Air",
    year: 2017
};
```
This defines a ChemECar object with 2 keys, `battery`, `year`, and 2 corresponding values, a `"Zinc-Air"` string and a `2017` number.

## Console.Log
We can access the properties of an object in different ways. If you're using Chrome, press Ctrl+Shift+I to open the console. We can use the `console.log` function to debug our program. For example, the following 2 lines of code are both equivalent and can be used to access the value stored by the `battery` key and will show 'Zinc-Air' in your console.

```javascript
console.log(ChemECar.battery)  //dot notation
console.log(ChemECar['battery'])  //bracket notation
```

Further reading:
1. http://www.w3schools.com/js/js_object_definition.asp
2. http://javascript.info/tutorial/objects

# 1. Load the jQuery Library
To begin, we will need to embed the jQuery library in our HTML file. We will grab the jQuery library from Google's CDN instead of loading the script locally. [Read this short article](http://robertgreiner.com/2011/05/using-a-content-delivery-network-to-host-jquery/) for further information on CDNs (Content Delivery Network) and its advantages.

1. Copy and paste this inside the `<head>` element of your index.html file. 
```javascript
<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.1.1/jquery.min.js"></script>
```

The first few lines of your file should now look something like this:
```html
<html>
<head>
<title> My first webpage </title>
<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.1.1/jquery.min.js"></script>
</head>
<body>
...
```

# 2. Understand the jQuery $.get Request
To begin, we will make a [GET request](http://www.w3schools.com/tags/ref_httpmethods.asp) to the Molson API using jQuery. 

The [jQuery documentation](https://api.jquery.com/jquery.get/) provides an example for using the get() function.
```javascript
$.get( "someURLWithData", function( data ) {
  $( selector ).html( data );
  console.log( data );
});
```
1. someURLWithData has some data that we make a 'GET request' for, in our case, this is the Molson API.
2. The data from the GET request is returned in `data`.
3. The jQuery `selector` selects elements such as `<div>` or `<p>`. It can also be specific elements if defined using IDs such as `<div id="SomeID">` that we target. 
4. `$( selector ).html(data)` replaces the HTML code in the element defined by the selector with the value stored in `data`.

In our case, we will define an ID for our element where we want the data to appear in, as follows:

```html
<p id="molsonData">Grabbing data...</p>
```

Our element selector would replace 'Grabbing data...' with our data from the Molson API.

# 3. Code it all up
1. Create a paragraph element with an ID of "molsonData", e.g. `<p id="molsonData"></p>`
2. Create a script with the type "text/javascript", e.g. `<script type="text/javascript"></p>`
3  Inside the script, make the GET request from `http://molson.ubcchemecar.com/api`.
4. Replace the selector with the chosen id along with a '#' sign in front of it. The '#' sign denotes an #ID for the selector. We can also have '.' for classes. IDs are unique elements in a HTML document, but multiple elements can have the same class. Further reading: http://www.w3schools.com/jquery/jquery_selectors.asp
5. Display the data in the console.log to check it.
6. Access the value stored in the timestamp key in `data` using `data.timestamp` or `data['timestamp']` and use our jQuery element selector to replace the HTML in #molsonData.

Your code should look something like this:
```javascript
    $.get( "http://molson.ubcchemecar.com/api", function( data ) {
      console.log(data)
      $("#molsonData").html( data['timestamp'] );
    });
```

We want to wait until the document has fully loaded before we start loading our script. So we enclose the above code in a `$( document ).ready()` block, or in shorthand jQuery notation, `$(function() {}`. Further reading: https://learn.jquery.com/using-jquery-core/document-ready/

The full code should look like this:
```html
<html>
<head>
<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.1.1/jquery.min.js"></script>
</head>
<body>
<p id="molsonData">Grabbing data...</p>
<script type="text/javascript">
  $(function() {
    $.get( "http://molson.ubcchemecar.com/api", function( data ) {
      console.log(data)
      $("#molsonData").html( data['timestamp'] );
    });
  });

</script>
</body>
</html>
```
## Overview
Essentially, what we did was: 

1. Get data from `http://molson.ubcchemecar.com/api`
2. Replace the code inside the element with id of "molsonData" with the newly acquired data. 
3. Specifically, the value in the `timestamp` key for this tutorial.

# Tutorial 3
Once you feel comfortable with the material here, move on to Tutorial 3 with the link below. As always, ask questions if you're stuck!

Tutorial 3 - https://github.com/ubcchemecar/beginners-tutorial/blob/master/tutorial-3.md
