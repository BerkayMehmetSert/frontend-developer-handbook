<h1 align="center">CSS GRID CHEAT SHEET</h1>

**Table of contents**

- [Parents](#parents)
- [Children](#children)
- [Getting fancy](#getting-fancy)

---

## Parents

_ Properties to apply to the parent grid container element._

### `display: grid`

_Turn a parent, container element into a grid. Causes all children to flow into grid cells._

```css
.container {
    display: grid;
}
```

### `grid-template-columns`

_Define how the columns are measured & how many there are._

```css
.container {
    /* 3 columns, equal size */
    grid-template-columns: 1fr 1fr 1fr;
    /* 3 columns, different sizes */
    grid-template-columns: 20rem 1fr;
    /* Create 12 equal-width columns */
    grid-template-columns: repeat(12, 1fr);
}
```

### `grid-template-rows`

_Define how the rows are measured & how many there are._

```css
.container {
    /* 2 rows, equal size */
    grid-template-rows: 1fr 1fr;
    /* 2 rows, different sizes */
    grid-template-rows: auto 3rem;
    /* Create 6 equal-height rows */
    grid-template-rows: repeat(6, 1fr);
}
```

### `grid-template-areas`

_Creaye a series of named areas within the parent to move elements into._

```css
.container {
    /* 3 columns, 3 rows
     * Areas spanning more than 1 column/row
     */
    grid-template-areas:
  "masthead masthead toolbar"
  "main     main     sidebar"
  "footer   footer   sidebar";
}
```

### `gap, column-gap, row-gap`

_Create space like a margin between the columns/rows of the grid._

```css
.container {
    grid-gap: 1rem;
    grid-column-gap: 1rem;
    grid-row-gap: 1rem;
}
```

### `justify-content & align-items`

_Align the elements horizontally within the grid. `content` moves all the elements together as a group. `items` moves
each element individually within their area._

```css
.container {
    justify-content: center;
    align-items: center;
}
```

### `align-content & align-items`

_Align the elements vertically within the grid. `content` moves all the elements together as a group. `items` moves each
element individually within their area._

```css
.container {
    align-content: start;
    align-items: center;
}
```

### `place-content & place-items`

_Apply both `justify` and `align` at the same time._

```css
.container {
    place-content: start;
    place-items: end;
}
```

### `grid-auto-columns & grid-auto-rows`

_Define the size of automatically generated intrinsic rows & columns._

```css
.container {
    grid-auto-columns: 1fr;
    grid-auto-rows: 10rem;
}
```

### `grid auto-flow: dense`

_Attempt to tightly pack grid cells, even moving cells earlier in the order._

```css
.container {
    grid-auto-flow: dense;
}
```

## Children

_These properties are to be applied to the children of the grid parent container._

### `grid-column`

_Choose which column the element starts & finishes at._

```css
.container {
    /* Start at column line 2 */
    grid-column: 2;
    /* Start at line 2, go to line 6 */
    grid-column: 2 / 6;
    /* Start at line 2, go to last line */
    grid-column: 2 / -1;
    /* Start at line 2, span horizontally 3 rows */
    grid-column: 2 / span 3;
}
```

### `grid-row`

_Choose which row the element starts & finishes at._

```css
.container {
    /* Start at row line 2 */
    grid-row: 2;
    /* Start at line 2, go to line 6 */
    grid-row: 2 / 6;
    /* Start at line 2, go to last line */
    grid-row: 2 / -1;
    /* Start at line 2, span vertically 3 rows */
    grid-row: 2 / span 3;
}
```

### `grid-area`

_Assign the element to a specific area in the grid._

```css
.container {
    grid-area: sidebar;
}
```

### `justify-self`

_Move the element itself horizontally within its defined area._

```css
.container {
    justify-self: center;
}
```

### `align-self`

_Move the element itself vertically within its defined area._

```css
.container {
    align-self: center;
}
```

### `place-self`

_Apply both `justify-self` & `align-self` at the same time._

```css
.container {
    place-self: center;
}
```

## Getting fancy

_Automatic responsive columns._

```css
.container {
    grid-template-columns: repeat(auto-fit, minmax(min(15rem, 100%), 1fr));
}
```

### `display: contents`

_Use on a parent element to get its children onto the grid._

Be careful with accessibility—some browsers don’t fully support it.

```css
.container {
    display: contents;
}
```