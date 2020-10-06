# Web Layouts in HTML and CSS - Week 2

From week one, you know the basics of how a web page is displayed and functions. The content is in HTML, the styles are in CSS, and logic is in the JS. But, the sample HTML & CSS page displayed everything top-down. How do we position, center, and arrange elements on the page? CSS has the answer, but you need to understand a few different mechanisms that CSS uses.

## CSS Flows

### The CSS Box Model
Before you can fully understand how elements are positioned in groups, you need to know how CSS calculates and _renders_ (shows) individual elements. This is done through the _CSS Box Model_. [W3 Schools has an excellent guide to what the box model is.](https://www.w3schools.com/Css/css_boxmodel.asp).

Below, you'll see a description of three different ways CSS positions your elements. They are not mutually exclusive, which means you can combine different flows and mechanisms in one page. This can be beneficial when one flow suits a particular portion of your site well, but another would be better for another portion.

### Normal Flow `display: block | inline | inline-block`
Normal Flow is the default for any HTML page. In normal flow, _block elements_ stack on top of each other. _Inline block elements_ also exist, which can be placed next to other inline elements. For example, an inline element like a `span` placed inside a `p` (paragraph) will not break up the paragraph into different lines. HTML elements like `span` and `div` automatically default to inline-block and block displays automatically, but you can manually specify this with CSS (`display: inline-block` or `display: block`).

It is important to note that all elements in a flow layout has an attribute of `position: relative`, which allows them to render with respect to the flow of elements around them. In addition, they also have `float: left` to keep them stacking from left to right. You can change the flow of your elements to be from right to left by changing that attribute to `float: right`, or `clear: left | right | both` to remove this characteristic when working with different layouts.

### CSS Flexbox `display: flex`
CSS Flexbox is a powerful tool that can be used in conjunction with normal flow to create _responsive websites_. Responsive design means that you don't have to design a site for desktop, another site for mobile, etc. Flexbox makes it easier to adjust between screen sizes so you can write less CSS.

### CSS Grid `display: grid | inline-grid`
As the name suggests, the grid layout creates a grid in which elements are displayed. The attribute `display: grid` should be applied to a container, in which its child elements would be automatically displayed as grid elements. It is important to note that the child elements of a grid element do not follow a grid layout, which is expected since you rarely want nested grids.

For better demonstration, let us assume that we have a `.container` with the attribute `display: grid`, with child elements `.item`:
```html
<div class='container'>
  <div class='item'></div>
  <div class='item'></div>
  <div class='item'></div>
</div>
```
**Container `.container`**

You can define the dimensions of the grid container and its grid cells using attributes `grid-template-columns` and `grid-template-rows`:
```css
.container {
  grid-template-columns: 30% 20px auto 40px 50px;
  grid-template-rows: 1fr 2fr 40px 30px;
}
```
The code above creates a grid which contains 5 rows and 4 columns. The grid items (in our case 3) will fill from the cell in the top left corner to the right unless specified otherwise. Each column and each row is designated a dimension, of which `auto` and `fr` are special cases. `auto` allows that column/row to be assigned a size based on whatever space is left of the container. `fr` is a fractional unit which stands for a part of the available space. For example, in our case 70px of the row space is taken (40px + 30px). Since we have a total of 3fr in that space, the remaining row space (subtracting 70px) is divided into 3, of which 1/3 of the space is assigned to the first row and 2/3 to the second row.

Another powerful feature of a grid container is `grid-area`, which we will not cover here due to its complexity.

**Grid Item `.item`**

While a grid item normally occupies one grid cell, you can allow it to span across multiple columns and rows:
```css
.item {
  grid-column: 3 / span 3;
  grid-row: fifth-line / 7;
}
```
In this case, our item will occupy from the third column to the sixth column, and from the fifth row to the seventh row. This can also be expressed like so:
```css
.item {
  grid-column-start: 3;
  grid-column-end: 6;
  grid-row-start: 5;
  grid-row-end: 7;
}
```
An important distinction to be made is that a grid item is not the same as a _grid cell_. As the above example demonstrates, a grid item can spread across multiple cells. A grid item may also be smaller than a grid cell, which means it can be formatted with respect to the grid cell:
```css
.item {
  justify-self: start | end | center | stretch;
}
```
`start` aligns the item to the left of the cell, while `end` aligns it to the right and `center` aligns it to the center. `stretch` allows the item to cover the entire grid cell. There are other alignment attributes such as `align-self` and `place-self`. They are virtually the same as `justify-self`; their intricate differences are beyond the scope of this tutorial.
