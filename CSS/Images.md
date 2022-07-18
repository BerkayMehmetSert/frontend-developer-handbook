<h1 align="center">IMAGES CHEAT SHEET</h1>

**Table of Contents**

- [Image formats](#image-formats)
- [HTML tags](#html-tags)
- [HTML examples](#html-examples)
- [CSS background images](#css-background-images)
- [CSS gradients](#css-gradients)
- [Border images](#border-images)
- [Common CSS code snippets](#common-css-code-snippets)

---

## Image formats

### SVG

_Vector graphic_: Good for graphics with few colours, animations; can manipulate with code. Very scalable and retina
ready.

_Export settings_: Styling: Presentation attributes, Font: Convert to outline, Images: Link, Object IDs: Layer names,
Decimal: 1, Check minify, Uncheck responsive.

### PNG

_Raster graphic_: Good for graphics with few colours. PNG-24 has millions of colours & 256 levels of transparency.

PNG-8 has 256 colours—Photoshop’s implementation is incorrect, use ImageAlpha.

Not really retina capable: use SVG instead.

_Export settings_: Interlaced, Uncheck embed color profile, Internet Standard RGB, Metadata: None.

### JPG

_Raster graphic_: Good for photos and complex imagery.

_For retina_: determine max dimensions on website, double the original graphic size, compress to around 20%. Link inside
an SVG to get masks & transparency.

_Export settings_: Compression: ~65% (~20% for double-sized retina), Progressive, Uncheck embed color profile, Internet
Standard RGB, Metadata: None.

### Favicon

Small icons used in different places on browsers.

_ICO sizes_: 16×16, 32×32 & 48×48.

_PNG sizes_: 152×152, 144×144 (transparent).

### GIF

Limited to 256 colours, can be animated.

Try to avoid using.

Use only for animations but using video is still preferred.

## HTML tags

### `<img src="..." alt="...">`

For inserting content-related images.

Use the `alt="…"` to describe the image, blank alt for decorative images.

If a formatted description is needed use `aria-details="…"`

Use the `srcset="…"` & `sizes=""` attributes for responsiveness.

### `<figure>`

For images that need captions.

Use the `<img>` and `<figcaption>` tags inside.

Use only `<figure>` with a caption, or if the image can be removed from its location and still make sense, e.g. “Refer
to Figure 1”.

### `<picture>`

Used for art direction of responsive images: different crops on different screens, etc.

Needs the `<source>` and `<img>` tags inside.

## HTML examples

### `Image tag`

```html
<img src="pluto.jpg" alt="Photo of Pluto">
```

### `Figure`

```html

<figure>
  <img src="pluto.jpg" alt="">
  <figcaption>Photo of Pluto taken with the Hubble Telescope</figcaption>
</figure>
```

### `Favicons`

```html
<!-- .ico should have 16, 32, 48 px sizes -->
<link href="/favicon.ico" rel="shortcut icon">
<link href="/favicon-196.png" rel="icon" type="image/png">

<!-- Very optional -->
<meta name="application-name" content="Your Site Name">
<link rel="apple-touch-icon-precomposed" href="/favicon-196.png">
<meta name="msapplication-TileImage" content="/favicon-144.png">
<meta name="msapplication-TileColor" content="#ef0303">
```

### `Responsive & retina image tags`

```html
<img
  src="small.jpg"
  srcset="larage.jpg 2000w, medium.jpg 1000w, small.jpg 320w"
  sizes="(min-width: 38em) 50vw, 100vw"
  alt="A giant squid swimming deep in the sea"
>
```

### `Picture`

```html

<picture>
  <source media="(min-width: 60em)" srcset="high.jpg">
  <source media="(min-width: 35em)" srcset="medium.jpg">
  <img src="small.jpg" alt="A giant squid swimming deep in the sea">
</picture>
```

### `Retina picture`

```html

<picture>
  <source media="(min-width: 60em)" srcset="large@2x.jpg 2x, large.jpg 1x">
  <source media="(min-width: 35em)" srcset="medium@2x.jpg 2x, medium.jpg 1x">
  <img src="small.jpg" srcset="small@2x.jpg 2x, small.jpg 1x" alt="A giant squid swimming deep in the sea">
</picture>
```

## CSS background images

### `background-image`

```css
.background-image {
    background-image: url("image.jpg");
}
```

### `background-repeat`

```css
.background-repeat {
    /* Don’t repeat in either direction */
    background-repeat: no-repeat;
    /* Repeat only horizontally */
    background-repeat: repeat-x;
    /* Repeat only vertically */
    background-repeat: repeat-y;
    /* Get browser to determine how to repeat the image well */
    background-repeat: space;
    background-repeat: round;
}
```

### `background-position`

```css
.background-position {
    /* 10px in from the left, 25px down from the top */
    background-position: 10px 25px;

    /* Stuck to right side, in the vertical center */
    background-position: right center;

    /* Move up from the bottom with calc(): 25px up from the bottom */
    background-position: center calc(100% - 25px);
}
```

### `background-attachment`

```css
.background-attachment {
    background-attachment: fixed;
}
```

## CSS gradients

_Always provide a `background-color` when using gradients._

### `Gradients`

```css
.gradient {
    background-image: linear-gradient(to right, purple, indigo);
}
```

Angle the gradient by adjusting the first value:

```css
.gradient {
    background-image: linear-gradient(33deg, purple, indigo);
}
```

Also radial gradients, with the keywords `circle` or `ellipse` followed by a position:

```css
.gradient {
    background-image: radial-gradient(circle at center, purple, indigo);
}
```

### `Gradients with stops`

```css
.gradient {
    /* Two purples separated by a sharp black line */
    background-image: linear-gradient(33deg, purple 0%, purple 49%, black 49%, black 50%, indigo 50%);
}
```

### `Repeated gradients`

```css
.gradient {
    /* Black/yellow warning stripes */
    background-image: repeating-linear-gradient(45deg, yellow, yellow 10%, black 10%, black 20%);
}
```

## Border images

### `border-image-source`

```css
.border-image-source {
    border-image-source: url("../images/border.svg");
}
```

### `border-image-slice`

```css
.border-image-slice {
    /* 36px in from every edge */
    border-image-slice: 36px;
    /* 36px in from top/bottom; 24px in from left/right */
    border-image-slice: 36px 24px;
    /* 36px from top, 24px from right, 12px from bottom, 17px from left */
    border-image-slice: 36px 24px 12px 17px;
}
```

### `border-image-width`

```css
.border-image-width {
    /* 36px wide in every direction */
    border-image-width: 36px;
    /* 36px wide on top/bottom; 24px wide on left/right */
    border-image-width: 36px 24px;
    /* 36px wide top, 24px wide right, 12px wide bottom, 17px wide left */
    border-image-width: 36px 24px 12px 17px;
}
```

### `border-image-repeat`

```css
.border-image-repeat {
    /* Same in both directions */
    border-image-repeat: repeat;
    /* Round horizontally, space vertically */
    border-image-repeat: round space;
}
```

### `border-image-outset`

```css
.border-image-outset {
    border-image-outset: 12px 16px;
}
```

## Common CSS properties

### `Flexible images`

```css
.img-flex {
  display: block;
  width: 100%;
}
```

### `Image replacement`

```css
.image-replacement {
  overflow: hidden;
  direction: ltr;
  text-align: left;
  text-indent: 100%;
  white-space: nowrap;
}
```

### `Button gradient`

```css
.btn {
  display: inline-block;
  background-color: purple;
  background-image: linear-gradient(to bottom, purple, indigo);
  border-radius: 6px;
}
```