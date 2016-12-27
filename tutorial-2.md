# Welcome to Tutorial 2 - Javascript (JS)
Javascript is the programming language of webpages that allows users to access, manipulate and store data. This tutorial will be examining the process of getting data from another webserver (an API) and implementing into your own webpage using a library of JS known as 'jQuery'

# 1. Acquire the jQuery Library

1. Copy and paste: ```<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.1.1/jquery.min.js"></script>``` into the ```<head>``` element of the index.html file. 

# 2. Understand the jQuery $.get Request
The syntax of the .get request is:
```
$.get( "someURLWithData", function( data ) {
  $( ".result" ).html( data );
  alert( "Load was performed." );
})
```
# 3. Get data from a webserver
We will be using the jQuery syntax to get data from http://molson.ubcchemecar.com/ 

