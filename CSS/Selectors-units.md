<h1 align="center">SElECTORS & UNITS CHEAT SHEETS</h1>

**Table of content**

* [Selectors](#Selectors)
* [Pseudo classes](#Pseudo-classes)
* [Pseudo elements](#Pseudo-elements)
* [Interaction selectors](#Interaction-selectors)
* [Attribute selectors](#Attribute-selectors)
* [Colours](#Colours)
* [Units](#Units)
* [Unit rules](#Unit-rules)

---

## Selectors

### `Tag`

_Select all the tags of the same type._

``` css
html {}
h1 {}
p {}
```

### `.` —  Class

_Select an element that has a class._

``` css
.masthead {}
.nav {}
.contact {}
```

_There needs to be a matching class in the HTML:_

``` html
<header class="masthead">
  <nav class="nav">
    ⋮
  </nav>
</header>
```

### `#` — ID

_Select an element that has the ID._

``` css
#heading-1 {}
#github {}
#top {}
```

_There needs to be a matching ID in the HTML:_

``` html
<a id="top" href="#top">Top</a>
```

### `Space` — Descendant

_Select an element that’s a descendant of another element._

``` css
ul li {}
nav a {}
ul li {}
```

### `>` — Child

_Select an element directly inside another element._

``` css
ul > li {}
h1 > span {}
footer > .copyright {}
```

### `+` — Adjacent sibling

_Select an element immediately beside another element._

``` css
h1 + p {}
hr + p {}
li + li {}
```

### `~` — General sibling

_Select an element that’s at the same level._

``` css
p ~ p {}
h1 ~ p {}
dd ~ dt {}
```

### `[]` — Attribute

_Select an element by it’s attribute._

_Good for styling links differently if they’re external._

``` css
[data-state="active"] {}
[href^="http"] {}
[download] {}
```

## Pseudo classes

### `:first-child`

_Select the element when it’s the first inside its parent._

``` css
p:first-child {}
ul li:first-child {}
.person:first-child {}
```

### `:last-child`

_Select the element when it’s the last inside its parent._

``` css
li:last-child {}
p:last-child {}
.item:last-child {}
```

### `:nth-child`

_Select an element by it’s number._

_Good for zebra-striping table rows._

``` css
li:nth-child(2) {}
tr:nth-child(odd) {}
div:nth-child(5n) {}
```

### `:only-child`

_Select an element when it’s the only thing inside its parent._

``` css
li:only-child {}
```

### `:nth-last-child()`

_Select an element by it’s number, counting backwards from the end._

``` css
/* Third from the bottom */
li:nth-last-child(3) {}
```

### `:nth-of-type()`

_Select an element by it’s number, but only counting others that match—not all children._

``` css
/* Second <p> element in its parent */
p:nth-of-type(2) {}
```

### `:nth-last-of-type()`

_Select an element by it’s number, counting backwards from the end._

``` css
/* Second <p> from the bottom */
p:nth-last-of-type(2) {}
```

### `:first-of-type`

_Select an element that’s the first of its kind within its parent._

``` css
p:first-of-type {}
```

### `:last-of-type`

_Select an element that’s the last of its kind within its parent._

``` css
p:last-of-type {}
```

### `:only-of-type`

_Select an element when it’s the only child of its parent of a specific kind._

``` css
p:only-of-type {}
section div:only-of-type {}
```

### `:empty`

_Select an element it has no children._

``` css
ul:empty {}
```

### `:disabled`

_Select an element when its `disabled` attribute is set._

``` css
button:disabled {}
```

### `:checked`

_Select an `<input>` when its checked attribute is set._

``` css
input:checked {}
```

### `:target`

_Select an element when the URL matches its ID._

``` css
li:target {}
```

### `:not()`

_Select matching elements that do not match the selection inside the `()`._

``` css
p:not(.hidden) {}
input:not(:checked) {}
```

### `:target`

_Select an element whet the URL matches its ID._

``` css
li:target {}
```

## Pseudo elements

### `::before`

_A hidden element before the content of most elements._

``` css
blockquote::before {
  content: "“";
  font-size: 5rem;
}
```

### `::after`

_A hidden element after the content of most elements._

``` css
blockquote::after {
  content: "”";
  font-size: 5rem;
}
```

### `::first-letter`

_Select the first character in the text. Good for drop caps._

``` css
p::first-letter {}
```

### `::first-line`

_Select the first line of text._

``` css
p::first-line {}
```

### `::selection`

_Style an element when it’s selected. and highlighted._

``` css
::selection {
	background: #f00;
	color: #fff;
}
```

## Interaction selectors

### `:link`

_For styling a link that hasn't been visited._

``` css
a:link {}
```

### `:visited`

_For styling a link that has been visited._

``` css
a:visited {}
```

### `:hover`

_For styling an element when the mouse is over it._

``` css
a:hover {}
```

### `:active`

_For styling an element when the mouse button is clicked down on it._

``` css
a:active {}
```

### `:focus`

_For styling an element for when the keyboard focuses it.Only works on `<input>`, `<button>`, and form inputs by default._

``` css
input:focus {}
```

## Attribute selectors

### `Has an attribute`

_Select when an element has a specific attribute._

``` css
[download] {}
```

### `Exact match`

_Select when an attribute that's exactly the same._

``` css
[rel="stylesheet"] {}
```

### `Starts with`

_Select when an attribute starts with some text._

``` css
[href^="http://"] {}
```

### `Ends with`

_Select when an attribute ends with some text._

``` css
[src$=".jpg"] {}
```

### `Contains`

_Select when an attribute contains some text anywhere._

``` css
[class*="container"] {}
```

### `Contains when separated by spaces`

_Select an element when its attribute matches one item from a space separated list._

``` css
/*<p class="unit xs-1 s-1 m-1"></p>*/
[class~="s-1"] {}
```

### `Contains when separated by dashes`

_Select an element when its attribute matches one item from a dash separated list._

``` css
/*<p class="super-duper-long-class-name"></p>*/
[class|="duper"] {}
```

### `Case insesitive`

_Allows the search to ignore upper vs. lower case letters._

``` css
[lang|="en"] {}
```

## Colors

### `Keywords`

``` css
background-color: red;
color: darkorange;
border-color: hotpink;
```

### `Hexadecimal`

_Hex colours start with a hash: `#`._

``` css
background-color: #000000; 
color: #ff3333;
border-color: #b95f4;
outline-color: darkorange;
```

### `RGB`

_Specify colours using red, green & blue numbers._

``` css
background-color: rgb(255, 255, 255);
color: rgb(255, 0, 0);
border-color: rgb(124, 65, 99);
outline-color: rgb(255, 0, 0);
```
### `RGBA`

_RGB with semi-transparent/opacity._

``` css
background-color: rgba(0, 0, 0, .5);
color: rgba(255, 0, 0, .75);
border-color: rgba(124, 65, 99, .8);
outline-color: rgba(255, 0, 0, .5);
```

### `HSL`

_Specify colours using the hue, saturation, lightness system._

``` css
background-color: hsl(0, 100%, 100%);
color: hsl(53, 100%, 50%);
border-color: hsl(167, 38%, 59%);
outline-color: hsl(53, 100%, 50%);
```

### `HSLA`

_HSL with semi-transparent/opacity._

``` css
background-color: hsla(0, 100%, 100%, .5);
color: hsla(53, 100%, 50%, .7);
border-color: hsla(167, 38%, 59%, .3);
outline-color: hsla(53, 100%, 50%, .5);
```

### `Transparency`

_The `transparent` keyword can be used to remove a colour._

``` css
background-color: transparent;
```

### `Current colour`

_The `currentColor` keyword can be used to capture the `color` of the same element._

``` css
color: red;
border-color: currentColor; /* Will be red */
outline-color: currentColor; /* Will be red */
```

## Units

### `Pixels`

_CSS pixels—different sizes for every device.100px is exactly 100 pixels in all situations._

``` css
width: 100px;
height: 100px;
```

### `Em`

_Based on the font-size of the parent (or current element)._

``` css
font-size: 1.5em;
```

### `Rem`

_Based on the font-size of the `html` element._

``` css
font-size: 1.5rem;
```

### `Percentage`

_A percentage of the parent element._

``` css
width: 50%;
```

### `Viewport height`

_Like percentage, but based on the height of the window._

``` css
height: 100vh;
```

### `Viewport width`

_Like percentage, but based on the width of the window._

``` css
width: 100vw;
```