<h1 align="center">BOXES & BORDERS CHEAT SHEET</h1>

**Table of content**

- [The Box Model](#The-Box-Model)
- [Box dimensions](#Box-dimensions)
- [Colors & Borders](#Colors-&-Borders)
- [Box sizing systems](#Box-sizing-systems)
- [Display & Layout](#Display-&-Layout)

---

## The Box Model

_Starting at the content and working out._

- `padding` - space between the content & box edge.
- `border` - line around the edge of the box.
- `margin` - space outside the box, pushing other boxes away; can see through margin to what's behind.

`margin` & `padding` can take 1–4 values.

``` css
/* 10px on all four sizes of the box */
margin: 10px;
/* 10px top/bottom; 12px left/right */
margin: 10px 12px;
/* 10px top; 12px left/right; 14px bottom */
margin: 10px 12px 14px;
/* 10px top; 12px right; 14px bottom; 16px left */
margin: 10px 12px 14px 16px;

/* 10px on all four sizes of the box */
padding: 10px;
/* 10px top/bottom; 12px left/right */
padding: 10px 12px;
/* 10px top; 12px left/right; 14px bottom */
padding: 10px 12px 14px;
/* 10px top; 12px right; 14px bottom; 16px left */
padding: 10px 12px 14px 16px;
```

## Box dimensions

### `margin`

_Create space outside the box, pushing other boxes._

``` css
/* See above for examples of the value system */
margin: 1.125em;
margin: 1.125em 1em;
```

Target each side individually: `margin-top`, `margin-right`, `margin-bottom`, `margin-left`.

``` css
margin-top: 1.125em;
margin-right: 1.125em;
margin-bottom: 1.125em;
margin-left: 1.125em;
```

**Negative margins:**

``` css
margin-top: -1.125em;
margin-right: -1.125em;
margin-bottom: -1.125em;
margin-left: -1.125em;
```

### `padding`

_Create space inside the box, pushing text away from the edge._

``` css
/* See above for examples of the value system */
padding: 1em;
margin: 1em .8em;
```

Target each side individually: `padding-top`, `padding-right`, `padding-bottom`, `padding-left`.

``` css
padding-top: 1em;
padding-right: 1em;
padding-bottom: 1em;
padding-left: 1em;
```

### `width`

_Control the horizontal space of a box._

``` css
width: 100px;
width: 50%; /* of the element its inside */
width: 100vw; /* Full width of the window */
```

### `height`

_Controls the vertical space of a box._

``` css
height: 100px;
height: 50%; /* of the element its inside */
height: 100vh; /* Full height of the window */
```

### `min-width`

_Make a box be at least a certain width, but can expand._

``` css
min-width: 100px;
```

### `min-height`

_Make a box at least a certain height, but can expand._

``` css
min-height: 12em;
min-height: 75vh; /* 75% height of the window */
```

### `overflow`

_Control how elements that break out the edges of the box are dealt with._

One of: `visible`, `hidden`, `scroll`, `auto`.

``` css
overflow: hidden; /* Chop off everything */
overflow: auto; /* Introduce a scrollbar if necessary */
```

Also control a single direction: `overflow-x`, `overflow-y`.

``` css
overflow-x: hidden; /* Chop off everything */
overflow-y: auto; /* Introduce a scrollbar if necessary */
```

### `calc()`

_Sometimes we can’t calculate a value ahead of time because it depends on something the browser knows but we don’t, e.g. adding `em` + `px` together._

``` css
width: calc(100vw - 10px);
padding-left: calc(1.4em + 24px);
```

Always have a space around the math operator!

``` css
width: calc(100vw-10px); /* Not gonna work */
```

## Colors & Borders

### `color`

_Set the color of the text._

``` css
color: #fff;
color: rgba(255, 255, 255, 0.5);
```

### `background-color`

_Set the colour of the box, behind the text._

``` css
background-color: orange;
background-color: #e2e2e2;

/* Semi-transparent colour */
background-color: rgba(0, 0, 0, .5);
```

### `border-color`

_Set the colour of the box stroke._

``` css
border-color: indigo;
border-color: #f33;
```

### `border-width`

_Control the thickness of the stroke around a box._

``` css
border-width: 12px;

/* Or use em if you want it to scale with the text size */
border-width: .1em;
```

### `border-style`

_Set the visual appearance of the line._

Possible values: `none`, `solid`, `dashed`, `dotted`, `double`, `groove`, `ridge`, `inset`, `outset`.

``` css
border-style: solid;
border-style: dotted;
```

### `border (shorthand)`

_A short form version for setting the three border properties._

 border: `border-width` `border-style` `border-color`.

``` css
border: 3px solid black;
border: 4px dotted green;
```

Borders on single sides: `border-top`, `border-right`, `border-bottom`, `border-left`.

``` css
border-top: 3px solid indigo;
border-bottom: 3px solid indigo;
```

### `border-radius`

_Make the corners of the box slightly rounded._

``` css
border-radius: 4px;
border-radius: .3em;
```

Control each side differently, start on top-left, go clockwise around.

``` css
border-radius: 4px 6px 10px 12px;
```

Do ovals using a `/` to separate the different axes

``` css
border-radius: 4px/10px;
```

### `opacity`

_Make the whole box and all its content semi-transparent.A number between `0` & `1`._

``` css
opacity: .5;
opacity: .2;
```

### `box-shadow`

_Create a drop-shadow behind the box._

Requires at least 3 values: `offset-x`, `offset-y`, `blur-radius`.

``` css
box-shadow: 2px 2px black;
box-shadow: 2px 2px 10px rgba(0, 0, 0, .5);
box-shadow: 2px 2px 10px 4px rgba(0, 0, 0, .5);

/* Move the shadow inside the box with inset */
box-shadow: inset 2px 2px black;
```

Multiple box-shadows:

``` css
box-shadow: 2px 0 red, -2px 0 green;
```

### `outline`

_Like a border, but outside border, doesn’t take up space, will overlap surrounding elements._

``` css
outline: 2px solid black;
```

`outline-offset` — will push the outline away from the box edge.

``` css
outline-offset: 2px;
```

## Box sizing systems

### `box-sizing: content-box`

**Do not use `content-box`**

_The default box calculation math puts the padding & border outside the width set in CSS._

``` css
/*
  Total width of box is 130px:
  100px + 10px (left) + 10px (right) + 5px (left) + 5px (right) = 130px
*/
.box {
  width: 100px;
  padding: 10px;
  border-width: 5px;
}
```

### `box-sizing: border-box`

**Always use `border-box`**

_Simplifies the responsive math by making the width of a box, as set in CSS, not change by adding padding and border._

``` css
/* This snipped of CSS should always be included */
html {
  box-sizing: border-box;
}

*, *::before, *::after {
  box-sizing: inherit;
}
```

## Display & Layout

### `display:inline`

_Flows content together, fitting on the same line if possible._

`margin`, `padding`, `width` **don’t work**.

### `display: block`

_Takes up a whole line by itself._

`margin`, `padding`, `width` **do work**.

### `display: inline-block`

_A hybrid between `block` & `inline`: fits on the same line, allows `padding`, `width`, etc._

### `display: none`

_Completely hide the element from the page._

Set to another `display` value to make it visible again.