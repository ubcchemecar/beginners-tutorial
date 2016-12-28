# Welcome to Tutorial 2 - JavaScript (JS)
In this tutorial, we will be examining the process of getting data from another webserver (specifically, a [REST API](https://www.youtube.com/watch?v=7YcW25PHnAA)) and displaying the data your own webpage with the help of the `jQuery` library. `jQuery` is a JavaScript library that helps us write JavaScript code easier and faster using a simpler syntax. [Read this article](http://www.htmlgoodies.com/tutorials/forms/article.php/3895776/HTML-Forms-jQuery-Basics---Getting-Started.htm) for further information on jQuery. 

## HTML vs Javascript
HTML is a markup language designed for defining static web page content. JavaScript is a programming language designed for performing dynamic tasks. Further info: http://javascript.about.com/od/reference/p/javascript.htm 

In Tutorial 1, we used HTML to design a static website, in this tutorial, we will learn how to make our website more interactive by using JavaScript to retrieve, manipulate and display data. 


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

The data from the Molson API is in JSON (JavaScript Object Notation) format. JSON is essentially text (human-readable), but in a special format such that it can be easily converted into JavaScript objects. 

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

The syntax of the .get request is:
```javascript
$.get( "someURLWithData", function( data ) {
  $(selector).dataChange;
});
```
1. someURLWithData has some data that we make a 'GET request' for.
2. The response from the GET request is returned in `data`.
3. The selector is an element such as `<div>` or `<p>`, or it is an id such as `<div id="SomeID">` that we target
4. dataChange applies the requested data to the element or id.

# 3. Get data from a webserver
We will be using the jQuery syntax to get data from http://molson.ubcchemecar.com/api The data in this server is the time, temperature and pH in JSON format.

1. Create a paragraph element with the id of "molsonData". 
2. Create a script with the type "text/javascript".
3  Inside the script, make the get request from `http://molson.ubcchemecar.com/api`. Follow the syntax in step 2. and replace someURLWithData.
4. Replace the selector with the chosen id along with a '#' sign in front of it
5. replace data change to show '''.html(data['timestamp]');

The code should look like this:
```
$(function() {
    $.get( "http://molson.ubcchemecar.com/api", function( data ) {
      console.log(data)
      $("#molsonData").html( data['timestamp'] );
    });
});
```
In pseudocode, this reads: Please get data from `http://molson.ubcchemecar.com/api` and then replace the code in side the element with id of "molsonData" with the newly acquired data. Specifically, the timestamp data in this tutorial.


