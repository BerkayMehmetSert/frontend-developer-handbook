<h1 align="center">CSS LAYOUT CHEAT SHEET</h1>

**Table of Contents**

- [Layout mechanics](#layout-mechanics)
- [Centering elements](#centering-elements)
- [Common code](#common-code)

---

## Layout mechanics

### `display: inline`

_Allows other elements beside; margin, padding & width don’t work._

```css
.inline {
  display: inline;
}
```

### `display: block`

_Takes up an entire line; margin, padding & width work._

```css
.block {
  display: block;
}
```

### `display: inline-block`

_Allows other elements beside; margin, padding & width work. Can create columns, but will force a space between boxes._

```css
.inline-block {
  display: inline-block;
}
```

### `float: left|right|none`

_Allows other elements to wrap around the element._

```css
.float-left {
  float: left;
}
```

### `clear: left|right|both`

_Force the element floated elements._

```css
.clear-left {
  clear: left;
}
```

### `overflow: hidden`

_Use on a parent element to force it to wrap around the floated children - a clearfix._

```css
.clearfix {
  overflow: hidden;
}
```

### `position: absolute`

_Move an element around based on coordinates._

```css
.absolute {
  position: absolute;
}
```

### `position: relative`

_Added to a parent element to reset absolute child's coordinates._

```css
.relative {
  position: relative;
}
```

### `position: fixed`

_Forces an element to not move when the page is scrolled._

```css
.fixed {
  position: fixed;
}
```

### `z-index`

_Control the stacking order of elements—higher number is closer._
  
```css
.z-index {
  z-index: 1;
}
```

## Centering elements

### `text-align: center`

_Works only on `display: inline` & `inline-block` elements._

```html
<figure class="img-box">
  <img src="images/argentinosaurus.jpg" alt="">
  <figcaption>The mighty Argentinosaurus</figcaption>
</figure>
```

```css
.img-box {
  text-align: center;
}
```

### `margin: 0 auto`

_Works only on `display: block` elements._

```html
<div class="box"> Lorem ipsum dolor sit amet </div>
```

```css
.box {
  width: 24em; /* Without a width `auto` won’t work */
  margin-left: auto;
  margin-right: auto;
}
```

### `vertical-align: middle`

_Works only on `display: inline` & `inline-block` elements._

```html
<ul>
  <li>Pteranodon</li>
  <li>Quetzalcoatlus</li>
</ul>
```

```css
ul li {
  display: inline-block;
  vertical-align: middle;
}
```

### `centering absolute`

_Use `transform` & `50%` coordinates to center an absolutely positioned element._

```html
<div class="banner">
  <div class="content">
    <h1>Micropachycephalosaurus</h1>
    <p>Longest dinosaur name ever!</p>
  </div>
</div>
```

```css
.banner {
  position: relative;
}

.content {
  position: absolute;
  left: 50%;
  transform: translateX(-50%);
}
```

Or vertical centering too…

```css
.content {
  position: absolute;
  left: 50%;
  top: 50%;
  transform: translate(-50%, -50%);
}
```

### `centering with flexbox`

_Flex box has a bunch of different alignment classes—that are always applied to the parent._

```html
<div class="card">
  <h2>Edmontosaurus</h2>
  <a href="#">See the bones!</a>
</div>
```

```css
.card {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-content: center;
  align-items: center;
}
```

## Common code

### `border box`

_Used to change layout math for width & padding._

```css
html {
  box-sizing: border-box;
}

*, *::before, *::after {
  box-sizing: inherit;
}
```

### `Clearfix for float`

_Add to the parent elements of floats to force the parent to surround the floated element._

```css
.clearfix::after {
  content: " ";
  display: block;
  clear: both;
}
```

### `flexible images`

_Use `width` & `display` to make images flex to their parent’s size._
  
```css
img {
  display: block;
  width: 100%;
}
```