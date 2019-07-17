# Intro to Web Dev - Week 1

## Starting with HTML
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

JavaScript is much more complex than HTML and CSS and more difficult to grasp.
