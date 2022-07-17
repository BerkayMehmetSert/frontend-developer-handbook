<h1 align="center">WEB TYPOGRAPHY CHEAT SHEET</h1>

**Table of content**
- [Metrics](#Metrics)
- [Units](#Units)
- [Properties](#Properties)
- [Text flow columns](#Text-flow-columns)
- [Experimental properties](#Experimental-properties)

---

## Metrics

### `1rem, 100%, 16px`

_**Body copy size** — should never be smaller._

`110%` for large screens.

`120%` for extra large screens.

### `1.3 - 1.5`

_**Body line-height** - looser on the web._

`1.3` for small screens.

`1.4` for medium screens.

`1.5` for large screens.

### `30em - 40em`

_**Body maximum line-length** - Shorter on small screens is okay._

## Units

### `rem`

_Based on the font-size set in the `html` element `1.5rem is 1.5x the  html` element's font-size._

### `em`

_Based on the font-size of the parent(or current element)._

`1em` is 1x the parent's element's size.

`0.5em` is 0.5x the parent's element's size.

### `%`

_A percentage of the font-size of the parent element._

`80%` is to 80% of the parent's element's size.

### `vh`

_Allows you to change the typed size based on the height of the window._


### `vw`

_Allows you to change the typed size based on the width of the window._

### `px`

_CSS pixels - different size for every device._

`16ppx` is exactly 16 pixels in all situations.

## Properties

### `color`

_The color of the text._

``` css
color: #fff;
```

### `font-family`

_Change the typeface of the text._

``` css
font-family: 'Open Sans', sans-serif;
```

### `font-size`

_Change the size of the text._

``` css
font-size: 1.5rem;
```

### `font-weight`

_Change the weight of the text. (`bold`, `normal`, `400`, `700`)_

``` css
font-weight: 700;
```

### `font-style`

_Change the capitalization of the text. (`italic`, `normal`)_

``` css
font-style: italic;
```

### `line-height`

_Adjust the space line takes up, similar to leading_

``` css
line-height: 1.5;
```

### `text-align`

_Adjust the position of the text within its parent. (`left`)._

``` css
text-align: left;
```

### `text-decoration`

_Add a decoration to the text. (`underline`, `none`, `line-through`, `overline`)_

``` css
text-decoration: underline;
```

### `text-indent`

_Indent the first line of text._

``` css
text-indent: 1em;
```

### `text-transform`

_Change the capitalization of the text. (`uppercase`, `lowercase`, `capitalize`)_

``` css
text-transform: uppercase;
```

### `text-shadow`

_Add a shadow to the text._

``` css
text-shadow: 1px 1px 1px #000;
```

### `text-overflow`

_Determine what happens to the text if it's too wide for its box._

``` css
text-overflow: ellipsis;
```

### `list-style-type`

_Control the style of bullets on a list. (`none`, `disc`, `circle`, `square`, `decimal`, `lower-roman`, `upper-roman`, `lower-alpha`, `upper-alpha`, `lower-greek`, `lower-latin`, `upper-latin`, `armenian`, `georgian`, `cjk-ideographic`, `hebrew`, `katakana`, `hiragana`, `none`)_

``` css
list-style: none;
```

### `font`

_Shorthand property for specifying lots of font details._

``` css
font: 1.5rem/1.5 'Open Sans', sans-serif;
```

### `letter-spacing`

_Controls the space between the different letters._

``` css
letter-spacing: 1px;
```

### `word-spacing`

_Controls the space between the different words._

``` css
word-spacing: 1px;
```

### `white-space`

_Controls how the text wraps. (`normal`, `nowrap`, `pre`)_

``` css
white-space: nowrap;
```

### `word-wrap`

_Controls whether the browser is allowed to break really long words. (`normal`, `break-word`)_

``` css
word-wrap: break-word;
```

## Text flow columns

_For making text flow between a few columns._

### `column-count`

_Set to the number of columns wanted in the text block._

``` css
column-count: 2;
```

### `column-gap`

_Set the amount of space between the columns._

``` css
column-gap: 1rem;
```

### `column-rule`

_Create a vertical border between each column._

``` css
column-rule: 1px solid #000;
```

## Experimental properties

_These properties may not work in all browsers and may have a major performance impact._

### `hyphens`

_Control if the text will be hyphenated._

Usually requires `text-align: justify`, `none`, `auto`.

``` css
hyphens: auto;
```

### `font-kerning`

_Control a font’s built-in kerning metrics._

`none`, `normal`, `auto`

``` css
font-kerning: normal;
```

### `font-variant-ligatures`

_Control whether ligatures are used or not._

`none`,`normal`, `common-ligatures`, `contextual`

``` css
font-variant-ligatures: normal;
```

### `font-variant-numeric`

_Enable/disabled alternative glyphs for numbers & fractions._

`normal`, `ordinal`, `slashed-zero`, `oldstyle-nums`, `tabular-nums`

``` css
font-variant-numeric: normal;
```

### `font-variant-caps`

_Control whether small caps are used or not._

`normal`, `small-caps`

``` css
font-variant-caps: small-caps;
```

### `text-rendering`

_Controls a bunch of the `font-variant` properties automatically._

``` css
text-rendering: optimizeLegibility;
```