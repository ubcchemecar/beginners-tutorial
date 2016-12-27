# Welcome to Tutorial 2 - Javascript (JS)
Javascript is the programming language of webpages that allows users to access, manipulate and store data. This tutorial will be examining the process of getting data from another webserver (an API) and implementing into your own webpage using a library of JS known as 'jQuery'

# 1. Acquire the jQuery Library

1. Copy and paste: ```<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.1.1/jquery.min.js"></script>``` into the ```<head>``` element of the index.html file. 

# 2. Understand the jQuery $.get Request
The syntax of the .get request is:
```
$.get( "someURLWithData", function( data ) {
  $(selector).dataChange;
});
```
1. someURLWithData has some data that we make a 'get request' for.
2. Our function manipulates this data.
3. The selector is an element such as ```<div>``` or ```<p>```, or it is an id such as ```<div id="SomeID">``` that we target
4. dataChange applies the requested data to the element or id.

# 3. Get data from a webserver
We will be using the jQuery syntax to get data from http://molson.ubcchemecar.com/api Thedata in this server is the time, temperature and ph as a javascript object.

1. Create a paragraph element with the id of "molsonData". 
2. Create a script with the type "text/javascript".
3  Inside the script, make the get request from '''http://molson.ubcchemecar.com/api'''. Follow the syntax in step 2. and replace someURLWithData.
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
In pseudocode, this reads: Please get data from '''http://molson.ubcchemecar.com/api''' and then replace anything with the id of "molsonData" with ```html``` with the newly acquired data. Specifically, the timestamp data.


