# Intro to Web Dev - Week 1

## Starting with HTML
After going through the [Hack Club Workshop](https://hackclub.com/workshops/personal_website), you now know how to create a static website with all the basic HTML elements. Just as a reminder, here is the basic setup of every HTML file before you get started working:
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

<table>
<tr><td>HTML Tag</td><td>Description</td><td>Example Usage</td></tr>
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
</table>
