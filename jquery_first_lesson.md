# JQuery

## What is JQuery?

jQuery is a fast, small, and awesome JavaScript library that makes things like finding and manipulating HTML elements, event handling, animation much simpler than they would would be in plain javascript. Jquery is very easy to use and works across most modern web browsers. In an nutshell, it's a library that makes using javascript easier and more enjoyable! 

## Getting Started

### Step 1: Load JQuery
First, we need to get JQuery loaded up on to your page. Add JQuery to your HTML document using a script tag:

```html
<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.2.1/jquery.min.js"></script>
```

We do this at the bottom of the `<body>`:

```html
<!DOCTYPE html>
<html>
  <head>
    <title>My Website</title>
  </head>
  <body>
    
  <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.2.1/jquery.min.js"></script>
  </body>
</html>
```

### Step 2: Create and connect a javascript file

Create a new file where you'll be writing your custom jquery and javascript (you can call this file anything you want as long as it has a `.js` extension) 

```
touch application.js
```

Cpnnect it to your HTML document after loading JQuery, using a `<script>` tag:

```html
<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.2.1/jquery.min.js"></script>
<script src="application.js"></script>
```

### Step 3: Set up JQuery to wait for the "DOM Ready Signal"

> *What is the DOM ? When you open a web page in your browser, the browser retrieves the page’s HTML text and parses it. The browser builds up a model of the document’s structure and then uses this model to draw the page on the screen.*

We want our JQuery to run once all the HTML elements have been loaded. When that happens, the DOM sends out a signal saying I'M READY!!! We specify that we want to wait for that signal by adding our code inside of a `$(document).ready()` function inside our javascript file:

**`application.js`**

```js
$(document).ready(function(){
  // This code will run when the HTML is fully loaded
});
```
You're now fully set up and ready to write your custom JQuery!

## Selectors and Syntax

jQuery selectors are used to "find" (or select) HTML elements based on their name, id, classes, types, attributes, values of attributes and much more. Selection is based on the existing CSS Selectors (so think back to how you selected HTML elements when you learned css!). To select an element we use the **"$"** dollar sign syntax:

1. Start with a dollar sign
2. Open parentheses 
3. Using quotation marks, define the element you're looking for
4. Close parentheses

So to select an `<h1>` element:

```js
$('h1')
```

To select a `<p>` element:

```js
$('p')
```

To select a `<li>` element:

```js
$('li')
```

You get the point... 

## Selecting specific DOM elements using IDs and Classes

If we only use element selectors like `$('h1')` we will select **all** h1 elements inside the page. But sometimes we don't want to select every single element in the document, so how do we select a specific element?

We use **classes** and **ids**! In the same way that we can style elements with css, we can select them by targeting their classes and ids.

Let's look at the following website and its elements:

```html
<!DOCTYPE html>
<html>
  <head>
    <title>My Website</title>
  </head>
  <body>
    <h1>What I Love</h1>
    
    <p>I love cats</p>
    
    <h1>What I Eat</h1>
    
    <p class="food">My favorite food is salads</p>
    <p id="dessert">My favorite dessert is ice cream</p>
  
  </body>
</html>
```

In this HTML document we have: 

- 2 `<h1>` Elements
- 3 `<p>` Elements

### Selecting every element of a kind

Selecting all h1 elements:

```js
$('h1') // => this will select all h1 tags (2 elements selected)
```

### Selecting an specific element by its `class` (use "`.`" like in css )

Selecting a p element with a class of "food"

```js
$('.food') // => this will select the second p tag and omit the first and last p tags (1 element selected)
```


### Selecting an specific element by its `id` (use "`#`" like in css )

Selecting a p element with an id of "dessert"

```js
$('#dessert') // => this will select the third p tag and omit the first two p elements (1 element selected)
```

***NOTE:*** *You can also select elements inside other elements by using spaces.*

```js
$('.someClass p') // => This will select a 'p' element inside an element with a class of 'someClass'
```

## Modifying Elements

Once we have selected an element we can extract and/or modify its content by using different methods:

## `.text()`

With this method we can find out what text is inside of the selected element and also we can modify it.

Let's see how it works:

If you have a `<p>` element with a class of "food":

```html
<p class="food">My favorite food is salads</p>
```

and you select this element using JQuery,

```js
$('.food')
```

then use the `.text()` method to extract its text content:

```js
$('.food').text(); // => 'My favorite food is salads'
```

If you want to modify its text content you can just write a different string inside of the parentheses using quotation marks like this:

```js
$('.food').text('My favorite food is tacos');
```

Now if you reload the page your HTML will change to:

```html
<p class="food">My favorite food is tacos</p>
```

And that is how we select and modify text inside elements.


## `.css()`

You can retrieve and edit css properties of the selected element(s) by using this method.

Retrieve `<p>` tag color:

```js
$('p').css('color'); // => rgb(0, 0, 0) Black
```

Change `<p>` tag color to red:

```js
$('p').css('color', 'red'); // => this will change the color of the selected tag to red.
```

Awesome, right!? That's JQuery. In future lessons we will learn more about all the different methods we can use to make our website more dynamic and fun.

## Resources

* [JQuery Api](http://api.jquery.com/)
* [Code Academy's JQuery Lessons](https://www.codecademy.com/learn/jquery)
* [Try JQuery Course](http://try.jquery.com/)

