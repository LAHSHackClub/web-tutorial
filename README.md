# Intro to Web Dev - Week 1

## Starting with HTML `.html`
The term HTML stands for _HyperText Markup Language_, and is used to create a layout for all websites. After going through the [Hack Club Workshop](https://hackclub.com/workshops/personal_website), you now know how to create a static website with all the basic HTML elements. Just as a reminder, here is the basic setup of every HTML file before you get started working:
```html
<!DOCTYPE HTML>
<html>
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />

  <title>Title Here!</title>

  <link rel="stylesheet" type="text/css" href="main.css" />
</head>
<body>
  <!-- All your displayed content goes here -->
  <script src="index.js"></script>
</body>
</html>
```
This is just the basic setup of a website. You have to add your own elements to it! Check out the list below for all the elements you can use!

## HTML Elements

There are so many HTML elements that you can use, no one knows them all! You can view the complete list [here](https://www.w3schools.com/tags/). It is important to think of HTML Elements as _DOM_ elements, or elements in the _Document Object Model_. In this model, every element is a node in a tree structure, where one element may be nested in another element, like how all of your displayed elements are nested under `<body>`. Having this understanding of _nesting_ early on in your web development career can help you more easily manipulate elements later on with CSS and JavaScript.

## CSS `.css`

You may have gotten to CSS on the Hack Club Workshop. If you didn't, don't worry about it! The acronym CSS stands for _Cascade Style Sheets_, and they are used for styling your website. For example, if I want to change the color of all of my paragraph elements to pink, then I can write in my `main.css` file the following lines of code:
```css
p {
  color: pink;
}
```
Of course, there is so much more CSS can do! You can do animations, transitions, change the background of your website, blur an image, and more! You can learn more about them [here](https://www.w3schools.com/css/default.asp). In most cases, working with CSS takes intuition and trial and error, so don't worry if you can't memorize all of the style attributes!

<!-- <table>
<tr><td><b>HTML Tag</b></td><td><b>Description</b></td><td><b>Example Usage</b></td></tr>
<tr>
<td>

`<p>`

</td>
<td>Paragraph Element - Normal text; often used in subtitles and descriptions.</td>
<td>

```html
<p>Hello! I am a paragraph!</p>
```

</td>
</tr>
<tr>
<td>

`<h1>, <h2>, <h3>, <h4>, <h5>, <h6>`

</td>
<td>Header Elements - Paragraph headers and titles in order of importance.</td>
<td>

```html
<h1>I am a header!</h1>
<h2>I am a lower header...</h2>
```

</td>
</tr>
<tr>
<td>

`<a>`

</td>
<td>Hyperlink Element - Allow a text to redirect the user to a link. Use the "href" attribute to add a link to your text.</td>
<td>

```html
<a href="lahs.club">This is our main website!</a>
```

</td>
</tr>
<tr>
<td>

`<button>`

</td>
<td>Button Element - You know what a button is! A button is often used to trigger a JavaScript event, but we wil get to that later!</td>
<td>

```html
<button onclick="myFunction();">Click Me!</button>
```

</td>
</tr>
<tr>
<td>

`<div>`

</td>
<td>Content Division Element - Typically used for general purpose, like creating a box, or a positioned block of elements. This element defaults to "block" display.</td>
<td>

```html
<div>
  <h1>Block Title</h1>
  <p>Block Paragraph</p>
</div>
```

</td>
</tr>
<tr>
<td>

`<span>`

</td>
<td>Span Element - Serves the same purpose as div of grouping elements, but defaults to "inline-block" display, meaning that it will not create its own line.</td>
<td>

```html
<span>
  <h1>I am Inline!</h1>
  <p>Me too!</p>
</span>
```

</td>
</tr>
</table> -->

## JavaScript `.js`

JavaScript is much more expansive than CSS and HTML, having applications in web development, app development, database management, and more. Many popular frameworks, or programming models, are based off of JavaScript, including NodeJS and ElectronJS, a framework used to build Discord and Slack. We will get to the applications of JavaScript outside of web development in the future, but for front-end development, JavaScript is essential to building a dynamic website instead of a static one.

Throughout this tutorial, we will be using JQuery, a popular JavaScript library that simplifies DOM manipulation and dynamic styling. To get JQuery, you can simply use a _CDN_, or Content Delivery Network, that serves a library via the network instead of locally:

```html
<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.4.1/jquery.min.js"></script>
```

We will get to using JQuery later on. Before then, you should become more familiar with native JavaScript. Here are some examples to help you get started:

### Variables
JavaScript is dynamically typed, meaning that you do not have to specify the datatype of a variable when you are declaring one. However, you should still know the primitive data types:

```js
// Numbers
var integer = 123;        // Integers
var doubles = 123.456;    // Floats and Doubles. In most programming languages, these belong to a separate data type. However, JavaScript treats them as the same data type.
var infinity = Infinity;  // A special numerical value; often the result of 1/0
var notNumber = NaN;      // If you do something like "text" / 3, then JavaScript would allow you to do that, but tell you that the result is "Not a Number"

// Strings
var doubleQuotes = "Hello World!";
var singleQuotes = 'Hello World!'; // No different from double quotes
var backticks = `Hello World! 1 + 122 is ${1 + 122}, or ${integer}`; // Can be used to embed an expression or a variable

// Booleans
var trueStatement = true;
var falseStatement = false;
var condition = 3 < 1; // This evalutes to false

// Special Cases
var doesNotExist = null;    // When a variable does not exist
var noAssigned = undefined; // When a variable exists but does not have a value associated with it

typeof integer // You can use this operation to determine the type of a variable. In this case, this operation will return "number". This will be useful once you have variables with self-defined types

```
There are two more datatypes: object and symbol. Neither of these types are primitive datatypes.

<b>Object</b>: More complex data structures. This is often an "object" that you define, which can be treated as a type, but always be classified by JavaScript as belonging to the "object" type

<b>Symbol</b>: Unique identifiers for objects. You will be unlikely to encounter these until you become proficient in JavaScript.

There are three ways of defining variables in JavaScript:
```js
const constant = 0;      // A constant, meaning that this variable cannot be changed after declaration.
let blockScoped = 0;     // Block scoped. This means that if this variable is called before declaration under the same "scope," then your script would error and tell you that the variable does not exist.
var functionScoped = 0;  // Function scoped. This means that if this variable is called before declaration under the same "scope," then your script will simply tell you that the variable exists, but does not have a value assigned to it.
```
### Conditional Statements
Conditional Statements are something you use to trigger an event under certain conditions. For example, I can tell my script to say "Hi" if my name is "Leo", "Hello" if my name is "Leon", and "Hey" otherwise. Here is how you would accomplish that in JavaScript:
```js
if (name === "Leo") {
  console.log("Hi");
} else if (name === "Leon") {
  console.log("Hello");
} else {
  console.log("Hey");
}
```
There are several other ways of accomplishing the same task! You can use switches or ternary operators. Ternary operators are better for conditions that only have two outcomes: true or false, so we will use "Leo" or not for that example.
```js
// Swithces
switch(name) {
  case "Leo":
    console.log("Hi");
    break; // This statement is required at the end of every case in a switch statement
  case "Leon":
    console.log("Hello");
    break;
  default:
    console.log("Hey");
    break;
}

// Ternary Operator
console.log((name === "Leo") ? "Hi" : "Hey") // Prints out "Hi" if the name is Leo, otherwise "Hey"
```

### Functions
Functions are extremely important when it comes to front-end development, because dynamic events such as a button click relies on calling a function once they are triggered. A function is essentially a sequence of tasks that will be executed once the function is called. There are several ways of defining a function in JavaScript:
```js
// The most common form of function declaration. You can declare this function after it is called.
function myFunction(a, b) {
  return a + b;
}

// This is called a function expression. If you call this function before it is called, you will get TypeError: myFunction is not a function.
var myFunction = function (a, b) {
  return a + b;
}

// This is called an arrow function. It wlil also error if called before the declaration. This type of function is most commonly seen in asynchronous handling and function mapping, which are beyond the scope of this tutorial.
var myFunction = (a, b) => {
  return a + b;
}
```

That's it with the basics! We will not get into more advanced stuffs such as classes and JSON data structure until later in the tutorial. Make sure you are familiar with these concepts before moving on!
