<h1 align="center">FLEXBOX CHEAT SHEET</h1>

**Table of content**

- [Enabling](#Enabling)
- [Orientation](#Orientation)
- [Alignment](#Alignment)
- [Flexibility](#Flexibility)

---

## Enabling

### `display: flex`

_Turns a parent element into a flex container-all child elements will become part of the flex flow._

Forces the parent element into a `display: block`-like state where it takes up an entire row.

``` css
.container {
	display: flex;
}
```

### `display: inline-flex`

_Same as `flex` but allows the parent element to be  `display: inline-block`._

``` css
.container {
	display: inline-flex;
}
```

## Orientation

### `flex-direction`

`row`, `row-reverse`, `column`, `column-reverse`

_Choose the direction of the flexbox children, horizontally (`row`) or vertically (`column`)._

``` css
.container {
	flex-direction: row;
}
```

### `flex-wrap`

`nowrap`, `wrap`, `wrap-reverse`

_Whether to allow the child elements to wrap to another line or force them all on a single line._

``` css
.container {
	flex-wrap: wrap;
}
```

### `order`

_Reorder a single child element within the flex flow._

``` css
.container {
	order: -1;
}
.container-2 {
	order: 2;
}
```

## Alignment

### `justify-content`

`flex-start`, `flex-end`, `center`, `space-between`, `space-around`

_Control how the elements are spaced within their parent flex container._

``` css
.container {
	justify-content: center;
}
```

### `align-items`

`flex-start`, `flex-end`, `center`, `baseline`, `stretch`

_Control how elements are aligned in the opposite direction of their justification._

``` css
.container {
	align-items: center;
}
```

`align-self` — is a similar property, but allows you to target a single child element, instead of all of the children.

``` css
.container {
flex-direction: row;
  align-self: flex-end;
}
```

### `align-content`

`flex-start`, `flex-end`, `center`, `space-between`, `space-around`, `stretch`

_How to align the grouping of wrapped flex children—only works with `flex-wrap: wrap`._

``` css
.container {
	align-content: center;
}
```

## Flexibility

### `flex-basis`

_Similar to `width` and `height` but not a guaranteed size: it can adjust up or down within the flex-parent to make sure the elements fit. It’s more like a suggestion._

``` css
.container {
	flex-basis: 50%;
}
```

### `flex-grow`

_A unitless number that defines how much of the leftover space this element should be allotted. Chunks the leftover space and allots based on this multiplier._

Without `flex-grow` all elements will be allotted the same amount of space.

``` css
.container {
	flex-grow: 1;
}
```

### `flex-shrink`

_Opposite to `flex-grow`: defines how much space it can shrink. If it can shrink. If there isn’t enough space available the element will remove allotments against this multiplier.._

``` css
.container {
	flex-shrink: 1;
}
```