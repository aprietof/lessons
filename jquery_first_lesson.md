# JQuery

## What is JQuery?

jQuery is a fast, small, and awesome JavaScript library. It makes things like finding and manipulating HTML elements, event handling, animation much simpler, it is very easy to use and works across a multitude of browsers. Basically, it's a library that makes using javascript way easier! (write less code and do more)


## Getting Started

### Step 1
Add JQuery to your HTML document A.K.A **"The DOM"** using a script tag.

```html
<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.2.1/jquery.min.js"></script>
```

At the bottom of the body.


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

### Step 2

Create a new file for your javascript (you can call this file anything you want as long as it has a `.js` extension) 

```
touch application.js
```

add it to your HTML document after the JQuery script tag

```html
<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.2.1/jquery.min.js"></script>
<script src="application.js"></script>
```

### Step 3 
### Set up JQuery to wait for the "DOM Ready Signal"

We want our JQuery to run once all the HTML elements have been loaded, when that happens the DOM sends out a signal saying I'M READY!!! We specify that we want to wait for that signal by adding our code inside of a document ready function inside our javascript file:

**`application.js`**

```js
$(document).ready(function(){
  // code here
});
```

## Selectors and Syntax
jQuery selectors are used to "find" (or select) HTML elements based on their name, id, classes, types, attributes, values of attributes and much more. It's based on the existing CSS Selectors. To select an element we use the **"$"** dollar sign syntax:

1. Start with a dollar sign
2. Open parenthesis 
3. Using quotation marks we define the element
4. Close parenthesis

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

## Selecting specific DOM elements using ID and Classes

If we only use element selectors like `$('h1')` we will select all h1 elements inside the page, sometimes we don't want to select every single element in the document, so how do we select an specific element?

Well, we use classes and ids, the same way we did to style elements with css we can select them by targeting their classes and ids.

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

## Modifying Elements

Once we have selected an element we can extract and/or modify its content by using different methods:

## `.text()`

With this method we can find out what text is inside of the selected element and also we can modify it.

Let's see how it works:

If you have a p element:

```html
<p>I love cats</p>
```

and you select this element using JQuery,

```js
$('p')
```

then use the `.text()` method to extract its text content:

```js
$('p').text(); // => 'I love cats'
```

If you want to modify its text content you can just write a different string inside of the parenthesis using quotation marks like this:

```js
$('p').text('I love Dogs');
```

Now if you reload the page your HTML will change to:

```html
<p>I love Dogs</p>
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

Awesome right!? That's JQuery. In future lessons we will learn more about all the different methods we can use to make our website more dynamic an fun.

## Resources

* [JQuery Api](http://api.jquery.com/)
* [Code Academy's JQuery Lessons](https://www.codecademy.com/learn/jquery)
* [Try JQuery Course](http://try.jquery.com/)

