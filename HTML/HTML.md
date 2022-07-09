<h1 align="center">HTML GUIDE</h1>

> _Free guide to HTML. It features all elements and attributes._

**Guideline:**

> * ✅ : Yes
> * ⛔ : No
> * ❗  : Required
> * ⚠️ : Experimental

**Table of content**
- [a](#a)
- [abbr](#abbr)
- [address](#address)
- [area](#area)
- [article](#article)
- [aside](#aside)
- [audio](#audio)
- [b](#b)
- [base](#base)
- [bdi](#bdi)
- [bdo](#bdo)
- [blockquote](#blockquote)
- [body](#body)
- [br](#br)
- [button](#button)
- [canvas](#canvas)
- [caption](#caption)
- [cite](#cite)
- [code](#code)
- [col](#col)
- [colgroup](#colgroup)
- [data](#data)
- [datalist](#datalist)
- [dd](#dd)
- [del](#del)
- [details](#details)
- [dfn](#dfn)
- [dialog](#dialog)
- [div](#div)
- [dl](#dl)
- [dt](#dt)
- [em](#em)
- [embed](#embed)
- [fieldset](#fieldset)
- [figcaption](#figcaption)
- [figure](#figure)
- [footer](#footer)
- [form](#form)
- [h1](#h1)
- [h2](#h2)
- [h3](#h3)
- [h4](#h4)
- [h5](#h5)
- [h6](#h6)
- [head](#head)
- [header](#header)
- [hgroup](#hgroup)
- [hr](#hr)
- [html](#html)
- [i](#i)
- [iframe](#iframe)
- [img](#img)
- [input](#input)
- [ins](#ins)
- [kbd](#kbd)
- [label](#label)
- [legend](#legend)
- [li](#li)
- [link](#link)
- [main](#main)
- [map](#map)
- [mark](#mark)
- [meta](#meta)
- [meter](#meter)
- [nav](#nav)
- [noframes](#noframes)
- [noscript](#noscript)
- [ol](#ol)
- [optgroup](#optgroup)
- [option](#option)
- [output](#output)
- [p](#p)
- [picture](#picture)
- [pre](#pre)
- [progress](#progress)
- [q](#q)
- [rp](#rp)
- [rt](#rt)
- [rtc](#rtc)
- [ruby](#ruby)
- [s](#s)
- [samp](#samp)
- [script](#script)
- [section](#section)
- [select](#select)
- [small](#small)
- [source](#source)
- [span](#span)
- [strong](#strong)
- [style](#style)
- [sub](#sub)
- [summary](#summary)
- [sup](#sup)
- [table](#table)
- [tbody](#tbody)
- [td](#td)
- [template](#template)
- [textarea](#textarea)
- [tfoot](#tfoot)
- [th](#th)
- [thead](#thead)
- [time](#time)
- [title](#title)
- [tr](#tr)
- [track](#track)
- [u](#u)
- [ul](#ul)
- [var](#var)
- [wbr](#wbr)

---

## `a` 

| Type   | Self-closing | 
|--------|--------------|
| Inline | ⛔            |

> Creates a **link** to a URL: a web page, a section within a page, an email address... Also called the `anchor` element, where the `a` comes from.

_Example:_

```html
<a href="https://site.com">HTML</a>
```

### `href`
  
_Defines the target of the link. (❗)_

`href="https://site.com"` : You can pass an **absolute** URL.

`href="/element/div"` : You can pass a URL **relative** to the root domain.

`href="#footer"` : You can target an element within the same page. Here, we target the element `<div id="footer">`.

`href="mailto:alex@smith.com"` : You can use the `mailto` protocol. Clicking the link will open the user's email client.

### `target`

_Defines in which tab or window the clicked link will show up._

`target="_blank"` : Opens in a new browsing context, which is usually a **new tab**.

`target="_self"` : Opens in the current tab.

`target="_parent"` : Opens in the parent browsing context, or `_self` is there is none.

`target="_top"` : Opens in the top browsing context, or `_self` is there is none.

### `rel`

_Defines how the link target relates to the current web page._

`rel="nofollow"` : The target is not related. Used for external websites usually.

---

## `abbr`

| Type   | Self-closing | 
|--------|--------------|
| Inline | ⛔            |

> Defines an **abbreviation**, and usually includes its full description.

### `title`

_Displays the full description when hovering the element._

`title="HyperText Markup Language"`

---

## `address`

| Type  | Self-closing | 
|-------|--------------|
| Block | ⛔            |

> Defines a block for **contact information**.

_Example:_

```html
<address>
  Infinite Loop,<br>
  Cupertino, CA<br>
  95014, USA
</address>
```

---

## `area`

| Type   | Self-closing | 
|--------|--------------|
| Inline | ⛔            |

> Defines an interactive area within a `map`.

_Example:_

```html
<img src="/images/world-continents.png" width="320" height="160" orgwidth="320" orgheight="160" usemap="#world-continents">
<map name="world-continents">
  <area title="North America" href="https://en.wikipedia.org/wiki/North_America" shape="poly" coords="48,89,67,69,77,49,140,0,68,0,6,10,4,31,16,69">
  <area title="South America" href="https://en.wikipedia.org/wiki/South_America" shape="poly" coords="48,88,61,74,119,99,95,160,66,159">
  <area title="Europe" href="https://en.wikipedia.org/wiki/Europe" shape="poly" coords="124,49,145,46,158,50,187,43,198,6,146,1,115,21">
  <area title="Africa" href="https://en.wikipedia.org/wiki/Africa" shape="poly" coords="121,53,140,47,169,51,186,77,196,80,188,137,156,136,138,97,118,86">
  <area title="Asia" href="https://en.wikipedia.org/wiki/Asia" shape="poly" coords="166,50,184,77,201,74,215,91,258,108,263,87,283,74,297,8,192,3,191,29,187,46,170,42">
  <area title="Australia" href="https://en.wikipedia.org/wiki/Australia_(continent)" shape="poly" coords="257,107,263,85,314,89,316,137,294,151,249,132,248,114">
</map>
```

### `title`

_Defines the title of the area._

`title="North America"` : The title will appear when hovering the area.

### `shape`

_Defines the shape of the area._

`shape="rect"` : The shape is a rectangle and requires 4 coordinates.

`shape="circle"` : The shape is a circle and requires 2 coordinates and 1 radius.

`shape="polygon"` : The shape is a polygon with unlimited points.

### `coords`

_Defines the coordinates related to the shape_.

`coords="116,104,234,154"` : A `rect` requires two pairs `x1,y1,x2,y2`, where the first one defines the **top left** corner, and the second one the **bottom right** corner.

`coords="50,80,20"` : A `circle` requires a pair and a radius `x,y,r`. The pair defines the **center** of the circle.

`coords="198,374,243,303,428,387,361,624,296,624"` : A `polygon` requires a collection of `x,y` pairs.

### `href`

_Defines the target of the area._

`href="https://site.com"` : You can pass an **absolute** URL.

`href="/element/div"` : You can pass a URL **relative** to the root domain.

`href="#footer"` : You can target an element within the same page. Here, we target the element `<div id="footer">`.

`href="mailto:alex@smith.com"` : You can use the `mailto` protocol. Clicking the link will open the user's email client.

### `target`

_Defines in which tab or window the clicked area will show up._

`target="_blank"` : Opens in a new browsing context, which is usually a **new tab**.

`target="_self"` : Opens in the current tab.

`target="_parent"` : Opens in the parent browsing context, or `_self` is there is none.

`target="_top"` : Opens in the top browsing context, or `_self` is there is none.

---

## `artile` 

| Type  | Self-closing | 
|-------|--------------|
| Block | ⛔            |

> Defines a `self-contained` block of content that can exist in any context.
It can have its own header, footer, sections... Useful for a list of blog posts.

_Example:_

```html
<article>
  <header>
    <h3>
      <a href="/my-blog-post">My blog post</a>
    </h3>
  </header>
  <section>
    <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec viverra nec nulla vitae mollis.</p>
  </section>
  <footer>
    <small>
      Posted on <time datetime="2017-04-29T19:00">Apr 29</time> in <a href="/category/code">Code</a>
    </small>
  </footer>
</article>
```

---

## `aside`

| Type  | Self-closing | 
|-------|--------------|
| Block | ⛔            |

> Defines a block of content that is related to the main content. Displayed as a sidebar usually.

_Example:_

```html
<main>
  <h1>My blog post</h1>
  <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec viverra nec nulla vitae mollis.</p>
  <p>etc.</p>
</main>

<aside>
  <h3>About the author</h3>
  <p>Frontend Designer from Bordeaux, currently working for Improbable in sunny London.</p>
</aside>
```

---

## `audio` 

| Type  | Self-closing | 
|-------|--------------|
| Block | ⛔            |

> Allows to embed an audio clip into a web page.

_Example:_

```html
<audio src="/assets/Hal.mp3" controls></audio>
```

### `src`

_Defines the source of the audio file. (❗)_

`src="/assets/Hal.mp3"`: You can use a **relative** path.

### `volume`

_Set the volume. Between`0.0` (silent) and `1.0` (loudest)._

`volume="0.0"` : The track is **silent**.

`volume="1.0"` : The track is set to the **loudest**.

### `autoplay` 

_The track will automatically start on load. (No value required)_

### `controls`

_Show the browser's built-in audio controls. (No value required)_

### `loop`

_The track will loop when reaching the end. (No value required)_

### `muted`

_The track will be muted by default. (No value required)_

### `preload`

_The track will be preloaded when the page loads. (No value required)_

---

## `b`

| Type   | Self-closing | 
|--------|--------------|
| Inline | ⛔            |

> Makes an element **bold**.

_Example:_

```html
Hello <b>World</b>!
```

---

## `base`

| Type | Self-closing | 
|------|--------------|
|      | ✅            |

> Defines the base URL for all relative links of a web page. Should be placed in the `<head>`. 

_Example:_

```html
<base href="https://site.com">
<a href="/element/base">The HTML base element</a>
```

### `href`

_Defines the base target of all links of the web page._

`href="https://site.com"` : You can pass an **absolute** URL.

### `target`

_Defines in which tab or window the clicked link will show up._

`target="_blank"` : Opens in a new browsing context, which is usually a **new tab**.

`target="_self"` : Opens in the current tab.

`target="_parent"` : Opens in the parent browsing context, or `_self` is there is none.

`target="_top"` : Opens in the top browsing context, or `_self` is there is none.

---

## `bdi`

| Type   | Self-closing | 
|--------|--------------|
| Inline | ⛔            |

> Allows to display part of a text in the opposite direction. Stands for `bidirectional isolation`.

_Example:_

```html
The word <bdi>مرحبا</bdi> means "Hello" in Arabic.
```

---

## `bdo`

| Type   | Self-closing | 
|--------|--------------|
| Inline | ⛔            |

> Allows to override the direction of text. 

_Example:_

```html
The word <bdo dir="rtl">Hello</bdo> is "Hello" spelled backwards. 
```

### `dir`

_Defines in which direction the text should go._

`dir="rtl"` : The text goes from right to left.

`dir="ltr"` : The text goes from left to right.

---

## `blockquote`

| Type  | Self-closing | 
|-------|--------------|
| Block | ⛔            |

> Defines a **long quotation**.

_Example:_

```html
<blockquote cite="https://en.wikiquote.org/wiki/Marie_Curie">
  Be less curious about people and more curious about ideas.
</blockquote>
```

### `cite` 

_Defines the source URL of the quotation._

`cite="https://en.wikiquote.org/wiki/Marie_Curie"` : Defines the source URL of the quotation.

---

## `body`

| Type  | Self-closing | 
|-------|--------------|
| Block | ⛔            |

> The container for a web page's content. Must be a direct child of `<html>`, and must be an ancestor of all HTML elements (except where noted).

_Example:_

```html
<!DOCTYPE html>
<html>
  <head>
    <!-- Document metadata -->
  </head>
  <body>
    <!-- Document content -->
  </body>
</html>
```

---

## `br`

| Type   | Self-closing | 
|--------|--------------|
| Inline | ✅            |

> Defines a **line break** within a text.

_Example:_

```html
Lorem ipsum dolor sit<br>amet, consectetur adipiscing elit. Donec viverra<br>nec<br>nulla vitae mollis.
```

---

## `button`
| Type   | Self-closing | 
|--------|--------------|
| Inline | ⛔            |

> Defines a **clickable** button.

_Example:_

```html
<button>
  Submit form
</button>
```

### `name`

_Defines the unique identifier for that button within the form. It allows the server to access each button's value when submitted._

`name="submit_button"` : The name value must be unique within the context of a `<form>` container.
It can only contain alphanumeric characters `a-z A-Z 0-9` and some special characters like `- _…` but no space.

### `value`

_The value sent to the server when submitting the form._

`value="primary"` : The server will receive the value `primary`.

### `type`

_Defines the button type._

`type="submit"` : The button sends the form data to the server.

`type="reset"` : The button resets the form.

### `disabled`

_Disables the button. (No value required)_

### `autofocus`

_Sets focus on the element when the web page loads. (No value required)_

---

## `canvas`

| Type  | Self-closing | 
|-------|--------------|
| Block | ⛔            |

> Defines an element where you can draw **graphics**.

_Example:_

```html
<canvas>
  Fallback text for non-supported browsers
</canvas>
```

### `width`

_Defines the width of the canvas._

`width="200"` : Default is 100.

### `height`


_Defines the height of the canvas._

`height="50"` : Default is 150.

---

## `caption`

| Type  | Self-closing | 
|-------|--------------|
| Block | ⛔            |

> Defines the title of a `<table>`.

_Example:_

```html
<table>
  <caption>The Beatles</caption>
  <tr>
    <td>John Lennon</td>
    <td>Rhythm Guitar</td>
  </tr>
  <tr>
    <td>Paul McCartney</td>
    <td>Bass</td>
  </tr>
  <tr>
    <td>George Harrison</td>
    <td>Lead Guitar</td>
  </tr>
  <tr>
    <td>Ringo Starr</td>
    <td>Drums</td>
  </tr>
</table>
```

---

## `cite`

| Type   | Self-closing | 
|--------|--------------|
| Inline | ⛔            |

> Defines the source of a creative work.

_Example:_

```html
If you want to learn HTML and CSS, go read <cite>MarkSheet.io</cite>!
```

---

## `code`

| Type   | Self-closing | 
|--------|--------------|
| Inline | ⛔            |

> Defines a snippet of code within a block of text.

_Example:_

```html
Type <code>npm install</code> in your terminal to install a project's dependencies.
```

---

## `col`

| Type   | Self-closing | 
|--------|--------------|
| Inline | ✅            |

> Defines a **column** within a table.

_Example:_

```html
<table>
  <colgroup>
    <col style="background-color: hotpink;">
    <col span="2" style="background-color: springgreen;">
  </colgroup>
  <tr>
    <td>John Lennon</td>
    <td>Rhythm Guitar</td>
    <td>1960–1969</td>
  </tr>
  <tr>
    <td>Paul McCartney</td>
    <td>Bass</td>
    <td>1960–1970</td>
  </tr>
  <tr>
    <td>George Harrison</td>
    <td>Lead Guitar</td>
    <td>1960–1970</td>
  </tr>
  <tr>
    <td>Ringo Starr</td>
    <td>Drums</td>
    <td>1960–1970</td>
  </tr>
</table>
```

### `span`

_Defines how many columns the element should span._

`span="3"` : You can use numbers.

---

## `colgroup`

| Type  | Self-closing | 
|-------|--------------|
| Block | ⛔            |

> Defines a group of **columns** within a table. 

_Example:_

```html
<table>
  <colgroup>
    <col style="background-color: hotpink;">
    <col span="2" style="background-color: springgreen;">
  </colgroup>
  <tr>
    <td>John Lennon</td>
    <td>Rhythm Guitar</td>
    <td>1960–1969</td>
  </tr>
  <tr>
    <td>Paul McCartney</td>
    <td>Bass</td>
    <td>1960–1970</td>
  </tr>
  <tr>
    <td>George Harrison</td>
    <td>Lead Guitar</td>
    <td>1960–1970</td>
  </tr>
  <tr>
    <td>Ringo Starr</td>
    <td>Drums</td>
    <td>1960–1970</td>
  </tr>
</table>
```

---

## `data`

| Type   | Self-closing | 
|--------|--------------|
| Inline | ⛔            |

> Defines content linked to machine-readable output. 

_Example:_

```html
<p>Computers</p>
<ul>
  <li>
    <data value="499">Mini PC</data>
  </li>
  <li>
    <data value="899">Small laptop</data>
  </li>
  <li>
    <data value="1399">Large laptop</data>
  </li>
  <li>
    <data value="2099">Desktop PC</data>
  </li>
</ul>
```

### `value`

_The machine-readable output value._

`value="123"` : You can type any type value, like **numbers**.

`value="Hello World"` : You can also put **text**.

---

## `datalist`

| Type  | Self-closing | 
|-------|--------------|
| Block | ⛔            |

> Defines a list of **autocomplete** options when using a text `<input>`.

_Example:_

```html
<label>South American countries</label><br>
<input list="countries" placeholder="Type a country">

<datalist id="countries">
  <option value="Argentina">
  <option value="Bolivia">
  <option value="Brazil">
  <option value="Chile">
  <option value="Colombia">
  <option value="Ecuador">
  <option value="Guyana">
  <option value="Paraguay">
  <option value="Peru">
  <option value="Suriname">
  <option value="Uruguay">
  <option value="Venezuela">
</datalist>
```

---

## `dd`

| Type   | Self-closing | 
|--------|--------------|
| Inline | ⛔            |

> Defines an item in a **definition list**.

_Example:_

```html
<dl>
  <dt>Web</dt>
  <dd>The part of the Internet that contains websites and web pages</dd>
  <dt>HTML</dt>
  <dd>A markup language for creating web pages</dd>
  <dt>CSS</dt>
  <dd>A technology to make HTML look better</dd>
</dl>
```

---

## `del`

| Type   | Self-closing | 
|--------|--------------|
| Inline | ⛔            |

> Defines text that has been **deleted**.

_Example:_

```html
To write abbreviations, use the <del cite="https://developer.mozilla.org/en-US/docs/Web/HTML/Element/acronym">acronym</del> <ins>abbr</ins> HTML element.
```

### `cite`

_Defines the URL where the reason for the deletion is explained._

`cite="https://developer.mozilla.org/en-US/docs/Web/HTML/Element/acronym"` : You can only use a valid URL.

### `datetime`

_Defines when the deletion has occurred._

`datettime="2017-10-14T12:00:00.001-04:00"` : You need a valid datettime string.

---

## `details`

| Type  | Self-closing |
|-------|--------------|
| Block | ⛔            |

> Defines a toggable block of content with a summary and additional details.

_Example:_

```html
<details>
  <summary>Read more</summary>
  <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec viverra nec nulla vitae mollis.</p>
</details>
```

### `open`

_Defines whether the additional details are shown by default or not._

`open="true"` : The additional details are **visible** by default.

---

## `dfn`

| Type   | Self-closing |
|--------|--------------|
| Inline | ⛔            |

> Defines where a term is **defined** within a web page.

_Example:_

```html
The <dfn>World Wide Web</dfn> is the part of the Internet that uses the HTTP protocol.
```

---

## `dialog` ⚠️

| Type  | Self-closing |
|-------|--------------|
| Block | ⛔            |

> Defines a **dialog box** that can be opened and closed with JavaScript.

_Example:_

```html
<dialog>
  This is a dialog box!
</dialog>
```

### `open`

_Opens the dialog box by default.(No value required.)_

---

## `div`

| Type  | Self-closing |
|-------|--------------|
| Block | ⛔            |

> Defines a **generic block** of content, that does not carry any semantic value. Used for layout elements like containers.

---

## `dl`

| Type  | Self-closing |
|-------|--------------|
| Block | ⛔            |

> Defines a **definition list**.

_Example:_

```html
<dl>
  <dt>Web</dt>
  <dd>The part of the Internet that contains websites and web pages</dd>
  <dt>HTML</dt>
  <dd>A markup language for creating web pages</dd>
  <dt>CSS</dt>
  <dd>A technology to make HTML look better</dd>
</dl>
```

---

## `dt`

| Type | Self-closing |
|------|--------------|
|      | ⛔            |

> Defines a **definition term**.

_Example:_

```html
<dl>
  <dt>Web</dt>
  <dd>The part of the Internet that contains websites and web pages</dd>
  <dt>HTML</dt>
  <dd>A markup language for creating web pages</dd>
  <dt>CSS</dt>
  <dd>A technology to make HTML look better</dd>
</dl>
```

---

## `em`

| Type   | Self-closing |
|--------|--------------|
| Inline | ⛔            |

> Defines **emphasis** on text. Is usually rendered as _italic_ text.

_Example:_

```html
HTML should only be used to write <em>content</em>, and keep CSS for <em>styling</em> the web page.
```

---

## `embed`

| Type  | Self-closing |
|-------|--------------|
| Block | ⛔            |

> Defines a container for **external application**.

_Example:_

```html
<embed src="https://www.youtube.com/embed/kmk43_2dtn0" width="640" height="480">
```

### `src`

_Defines the source of the video._

`src="https://www.youtube.com/embed/kmk43_2dtn0"` : You can use a third-party video.

### `type`

_The MIME type of the application._

`type="video/mp4"` : You can use of the MIME types.

### `width`

_Defines the width of the container._

`width="150"` : The width in pixels.

### `height`

_Defines the height of the container._

`height="50"` : The height in pixels.

---

## `fieldset`

| Type  | Self-closing |
|-------|--------------|
| Block | ⛔            |

> Defines a **group of controls** within a form

_Example:_

```html
<form action="/subscribe" method="post">
  <fieldset>
    <legend>Subscribe to the Newsletter</legend>
    <input type="email" name="email">
    <button>Ok</button>
  </fieldset>
</form>
```

### `disabled`

_Disables the controls the fieldset contains.(No value required.)_

---

## `figcaption`

| Type  | Self-closing |
|-------|--------------|
| Block | ⛔            |

> Defines the **caption** of a **<figure>**. 

_Example:_

```html
<figure>
  <img src="/images/html-logo.png" alt="HTML logo">
  <figcaption>The HTML logo</figcaption>
</figure>
```

---

## `figure`

| Type  | Self-closing |
|-------|--------------|
| Block | ⛔            |

> Defines a single self-contained element, usually an image.

_Example:_

```html
<figure>
	<img src="/images/html-logo.png" alt="HTML logo">
</figure>
```

---

## `footer`

| Type  | Self-closing |
|-------|--------------|
| Block | ⛔            |

> Defines the **footer** of a web page or section.

_Example:_

```html
<footer>
  Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec viverra nec nulla vitae mollis.
</footer>
```

---

## `form`

| Type  | Self-closing |
|-------|--------------|
| Block | ⛔            |

> Defines an **interactive form** with controls.

_Example:_

```html
<form action="/signup" method="post">
  <p>
    <label>Title</label><br>
    <label>
      <input type="radio" name="title" value="mr">
      Mr
    </label>
    <label>
      <input type="radio" name="title" value="mrs">
      Mrs
    </label>
    <label>
      <input type="radio" name="title" value="miss">
      Miss
    </label>
  </p>
  <p>
    <label>First name</label><br>
    <input type="text" name="first_name">
  </p>
  <p>
    <label>Last name</label><br>
    <input type="text" name="last_name">
  </p>
  <p>
    <label>Email</label><br>
    <input type="email" name="email" required>
  </p>
  <p>
    <label>Phone number</label><br>
    <input type="tel" name="phone">
  </p>
  <p>
    <label>Password</label><br>
    <input type="password" name="password">
  </p>
  <p>
    <label>Country</label><br>
    <select>
      <option>China</option>
      <option>India</option>
      <option>United States</option>
      <option>Indonesia</option>
      <option>Brazil</option>
    </select>
  </p>
  <p>
    <label>
      <input type="checkbox" value="terms">
      I agree to the <a href="/terms">terms and conditions</a>
    </label>
  </p>
  <p>
    <button>Sign up</button>
    <button type="reset">Reset form</button>
  </p>
</form>
```

### `action`

_Defines which URL the form's information is sent to when submitted._

`action="/contact"` : You can use a **relative** URL.

`action="https://site.com/contact"`: You can use an **absolute** URL.

### `method`

_Defines the HTTP method used when submitting the form._

`method="post"` : The form information is sent to the server as part of the **request body**.

`method="get"` : The form information is sent to the server as part **URL parameters**: `/contact?first_name=Alex&last_name=Smith`.

### `name`

_The form's name when sent to the server. Useful when multiple forms are present on the same web page._

`name="sign_up_form"` : The name value must be unique within the context of the whole web page. It can only contain alphanumeric characters `a-z A-Z 0-9` and some special characters like `- _…` but no space.

### `autocomplete`

_Determines if the browser can autocomplete all the form's controls._

`autocomplete="on"` : The browser will **enable** autocomplete functions. This can however be overriden for each control individually. Try pressing "down" in this input. It will show previously entered email addresses.

 `autocomplete="off"` : The browser will **disable** autocomplete functions. This can however be overriden for each control individually.
 
### `target`

_Defines in which tab or window the clicked link will show up._

`target="_blank"` : Opens in a new browsing context, which is usually a **new tab**.

`target="_self"` : Opens in the current tab.

`target="_parent"` : Opens in the parent browsing context, or `_self` is there is none.

`target="_top"` : Opens in the top browsing context, or `_self` is there is none.

### `enctype`

_Defines the MIME type of the information sent to the server. Only works if the method is `post`._

`enctype="application/x-www-form-urlencoded"` : The default value.

`enctype="text/plain"` : For HTML5 plain text.

`enctype="multipart/form-data"` : Needed when using an `<input type="file">` element.

### `novalidate`

_Tells the browser to not validate the form on submission.(No value required.)_

---

## `h1` 

| Type  | Self-closing |
|-------|--------------|
| Block | ⛔            |

> Defines a section heading of level **one**: the highest level.

_Example:_

```html
<h1>My blog post</h1>
```

---

## `h2` 

| Type  | Self-closing |
|-------|--------------|
| Block | ⛔            |

> Defines a section heading of level **two**.

_Example:_

```html
<h1>My blog post</h1>
<p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec viverra nec nulla vitae mollis.</p>
<h2>Introduction</h2>
<p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec viverra nec nulla vitae mollis.</p>
```

---

## `h3` 

| Type  | Self-closing |
|-------|--------------|
| Block | ⛔            |

> Defines a section heading of level **three**.

_Example:_

```html
<h1>My blog post</h1>
<p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec viverra nec nulla vitae mollis.</p>
<h2>Introduction</h2>
<p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec viverra nec nulla vitae mollis.</p>
<h3>Example</h3>
<p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec viverra nec nulla vitae mollis.</p>
```

---

## `h4` 

| Type  | Self-closing |
|-------|--------------|
| Block | ⛔            |

> Defines a section heading of level **four**.

_Example:_

```html
<h1>My blog post</h1>
<p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec viverra nec nulla vitae mollis.</p>
<h2>Introduction</h2>
<p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec viverra nec nulla vitae mollis.</p>
<h3>Example</h3>
<p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec viverra nec nulla vitae mollis.</p>
<h4>Example</h4>
<p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec viverra nec nulla vitae mollis.</p>
```

---

## `h5` 

| Type  | Self-closing |
|-------|--------------|
| Block | ⛔            |

> Defines a section heading of level **five**.

_Example:_

```html
<h1>My blog post</h1>
<p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec viverra nec nulla vitae mollis.</p>
<h2>Introduction</h2>
<p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec viverra nec nulla vitae mollis.</p>
<h3>Example</h3>
<p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec viverra nec nulla vitae mollis.</p>
<h4>Example</h4>
<p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec viverra nec nulla vitae mollis.</p>
<h5>Example</h5>
<p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec viverra nec nulla vitae mollis.</p>
```

---

## `h6` 

| Type  | Self-closing |
|-------|--------------|
| Block | ⛔            |

> Defines a section heading of level **six**: the lowest level.

_Example:_

```html
<h1>My blog post</h1>
<p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec viverra nec nulla vitae mollis.</p>
<h2>Introduction</h2>
<p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec viverra nec nulla vitae mollis.</p>
<h3>Example</h3>
<p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec viverra nec nulla vitae mollis.</p>
<h4>Why</h4>
<p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec viverra nec nulla vitae mollis.</p>
<h5>Reason</h5>
<p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec viverra nec nulla vitae mollis.</p>
<h6>Focus</h6>
<p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec viverra nec nulla vitae mollis.</p>
```

---

## `head`

| Type  | Self-closing |
|-------|--------------|
| Block | ⛔            |

> Defines a container for a web page's **metadata**.

_Example:_

```html
<!DOCTYPE html>
<html>
  <head>
    <!-- Document metadata -->
  </head>
  <body>
    <!-- Document content -->
  </body>
</html>
```

---

## `header`

| Type  | Self-closing |
|-------|--------------|
| Block | ⛔            |

> Defines the **header** of a web page or section. 

_Example:_

```html
<header>
  <h1>HTML</h1>
  <nav>
    <a>Home</a>
    <a>About</a>
    <a>Contact</a>
  </nav>
</header>
```

---

## `hgroup` ⚠️

| Type  | Self-closing |
|-------|--------------|
| Block | ⛔            |

> Defines the **heading** of a section. It can only contain heading levels: `<h1>` `<h2>` `<h3>` `<h4>` `<h5>` `<h6>`.

_Example:_

```html
<hgroup>
  <h1>HTML</h1>
  <h2>Lorem ipsum dolor sit amet</h2>
</hgroup>
```

---

## `hr`

| Type | Self-closing |
|------|--------------|
|      | ✅            |

> Defines a **semantic** break between blocks of text. It is often represented as a **horizontal rule**.

_Example:_

```html
<p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec viverra nec nulla vitae mollis.</p>

<hr>

<h2>Next section</h2>
<p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec viverra nec nulla vitae mollis.</p>
```

---

## `html`

| Type  | Self-closing |
|-------|--------------|
| Block | ⛔            |

> Defines the **root** element of an HTML document. All other elements must be contained within this root element.

_Example:_

```html
<!DOCTYPE html>
<html>
  <head>
    <!-- Document metadata -->
  </head>
  <body>
    <!-- Document content -->
  </body>
</html>
```

---

## `i`

| Type   | Self-closing |
|--------|--------------|
| Inline | ⛔            |

> Makes an element **italic**.

_Example:_

```html
Hello <i>World</i>!
```

---

## `iframe`

| Type   | Self-closing |
|--------|--------------|
| Inline | ⛔            |

> Defines a container for a nested **browsing context**: you can include a web page _within_ another web page.

_Example:_

```html
<iframe src="https://site.com">
  Fallback text for non-supported browsers
</iframe>
```

### `src`

_Defines the URL of the nested web page._

`src="https://site.com"` :  You can type any URL. Be aware that some websites will not allow to be iframed.

### `width`

_Defines the width of the iframe._

`width="150"` : The width in pixels.

### `height`

_Defines the height of the iframe._

`height="50"` : The height in pixels.

### `allowfullscreen`

_Allows the browser to show the iframe in fullscreen with JavaScript.(No value required.)_

---

## `img`

| Type   | Self-closing |
|--------|--------------|
| Inline | ✅            |

> Defines an **image** inserted in the web page.

_Example:_

```html
<img src="/images/sunset.jpg" alt="Picture of a Ha Long Bay sunset">

<!-- For responsive images, use srcset and sizes -->

<img src="/images/sunset-360.jpg"
  alt="Picture of a Ha Long Bay sunset"
  srcset="/images/sunset-360.jpg 360w,
          /images/sunset-720.jpg 720w,
          /images/sunset-1440.jpg 1440w>"
  sizes="(min-width: 800px) 720px, 360px">
```

### `src`

_The URL where the image is hosted.(❗)_

`src="/images/tiramisu.jpg"` : You can use a **relative** URL.

`src="https://site.com/images/traffic.jpg"` : You can use an **absolute** URL.

### `alt`

_Alternative text to describe the image if it's not available. Used by screen readers.(❗)_

`alt="Picture of a Ha Long Bay sunset"` : Describe the image as if it was not present.

### `srcset`

_Defines a list of different **sources** for the same image. The browser will choose the best one to use._

`srcset="/images/sunset-@2x.jpg 2x"` : You can define a pixel density descriptor like `2x`. In this case, `sunset-@2x.jpg` is `720px` wide.

`srcset="/images/sunset-360.jpg 360w` : You can use a **width descriptor** like `360w`. This value is divided by one of the source sizes (defined in the sizes attribute) to obtain the **pixel density**.

### `sizes`

_Defines a list of different source **sizes**. You can combine each of them with a **media query**._

`sizes="(min-width: 800px) 1440px, 720px"` : The browser will use the `1440px` image (defined in srcset) if the viewport is larger than `800px`.
It will use the `720px` otherwise.

### `width`

_Defines the width of the image._

`width="720"` : The width in pixels.

### `height`

_Defines the height of the image._

`height="720"` : The height in pixels.

---

## `input`

| Type   | Self-closing |
|--------|--------------|
| Inline | ✅            |

> Defines an **interactive** control within a web form.

_Example:_

```html
<input type="text" name="first_name" placeholder="e.g. Alex">
```

### `type`
_Defines the type of form input.(❗)_

`type="text"` : Simple single line text input that accepts any type of character.

`type="email"` : Like a text input, but the browser will try to only allow valid email addresses.

`type="number"` : Like a text input, but the browser will try to only allow valid numbers.

`type="checkbox"` : A toggle checkbox that can only be one of two states: checked or unchecked. The value is only submitted by the form if the checkbox is checked.

`type="radio"`: Needs to be used used in combination with other radio buttons, so that they are mutually exclusive.

`type="submit"` : Submit button that is triggered when clicked or when pressing Enter.

### `name`

_Defines the unique identifier for that input within the form. It allows the server to access each input's value when submitted.(❗)_

`name="first_name"` : The name value must be unique within the context of a `<form>` container.

### `placeholder`

_Defines a non-selectable placeholder text that only appears when the input is empty._

`placeholder="e.g. Alex"` : You can hint at the format expected for the input.

### `required`

_Tells the browser that this input is **required**. Leaving it empty will show a warning.(No value required.)_

### `disabled`

_Disables the input.(No value required.)_

---

## `ins`

| Type   | Self-closing |
|--------|--------------|
| Inline | ⛔            |

> Defines text that has been **inserted**.

_Example:_

```html
To write abbreviations, use the <del cite="https://developer.mozilla.org/en-US/docs/Web/HTML/Element/acronym">acronym</del> <ins>abbr</ins> HTML element.
```

### `cite`

_Defines the URL where the reason for the deletion is explained._

`cite="https://developer.mozilla.org/en-US/docs/Web/HTML/Element/acronym"` : You can only use a valid URL.

### `datetime`

_Defines when the deletion has occurred._

`datettime="2017-10-14T12:00:00.001-04:00"` : You need a valid datettime string.

---
## `kbd`

| Type   | Self-closing |
|--------|--------------|
| Inline | ⛔            |

> Defines a snippet of **user input**.

_Example:_

```html
To save, press <kbd>Ctrl + S</kbd>.
```

---

## `label`

| Type   | Self-closing |
|--------|--------------|
| Inline | ⛔            |

> Defines a **label** for a form control.

_Example:_

```html
<label for="first_name">First name</label>
<br>
<input type="text" name="first_name" id="first_name">
```

### `for`

_Defines which control the label is associated with._

`for="last_name"` : Clicking the label will focus on the input with the `id` equal to `last_name`.

---

## `legend`

| Type  | Self-closing |
|-------|--------------|
| Block | ⛔            |

> Defines a **caption** for a parent's content.

_Example:_

```html
<form action="/subscribe" method="post">
  <fieldset>
    <legend>Subscribe to the Newsletter</legend>
    <input type="email" name="email">
    <button>Ok</button>
  </fieldset>
</form>
```

---

## `li`

| Type | Self-closing |
|------|--------------|
|      | ⛔            |

> Defines a list item within an ordered list `<ol>` or unordered list `<ul>`.

_Example:_

```html
<ol>
  <li>Step one</li>
  <li>Step two</li>
  <li>????</li>
  <li>PROFIT!!!</li>
</ol>

<p>My shopping list:</p>
<ul>
  <li>Milk</li>
  <li>Bread</li>
  <li>Chocolate</li>
  <li>More chocolate</li>
</ul>
```
---

## `link`

| Type | Self-closing |
|------|--------------|
|      | ⛔            |

> Defines a **link** between the current web page and an external link or resource.

_Example:_

```html
<link rel="stylesheet" type="text/css" href="./style.css">
```

### `href`

_Defines the target of the link. (❗)_

`href="https://site.com"` : You can pass an **absolute** URL.

`href="/style.css"` : You can pass a URL **relative** to the root domain.

### `rel`

_Defines a link type, explaining how the link relates to the current web page._

`rel="stylesheet"` : The link is a stylesheet.

`rel="icon"` : The link is a favicon.

`rel="author"` : The link is the web page's author website.

`rel="next"`: The link is the next page.

### `type`

_Defines the type of the linked resource._

`type="text/css"` : The link is an CSS file.

`type="text/html"` : The link is an HTML document.

---

## `main`

| Type  | Self-closing |
|-------|--------------|
| Block | ⛔            |

> Defines the **main content** of a web page. Can be displayed with a sidebar.

_Example:_

```html
<main>
  <h1>My blog post</h1>
  <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec viverra nec nulla vitae mollis.</p>
  <p>etc.</p>
</main>

<aside>
  <h3>About the author</h3>
  <p>Frontend Designer from Bordeaux, currently working for Improbable in sunny London.</p>
</aside>
```

---

## `map`

| Type  | Self-closing |
|-------|--------------|
| Block | ⛔            |

> Defines an **interactive** map over an image.

_Example:_

```html
<img src="/images/world-continents.png" width="320" height="160" orgwidth="320" orgheight="160" usemap="#world-continents">
<map name="world-continents">
  <area title="North America" href="https://en.wikipedia.org/wiki/North_America" shape="poly" coords="48,89,67,69,77,49,140,0,68,0,6,10,4,31,16,69">
  <area title="South America" href="https://en.wikipedia.org/wiki/South_America" shape="poly" coords="48,88,61,74,119,99,95,160,66,159">
  <area title="Europe" href="https://en.wikipedia.org/wiki/Europe" shape="poly" coords="124,49,145,46,158,50,187,43,198,6,146,1,115,21">
  <area title="Africa" href="https://en.wikipedia.org/wiki/Africa" shape="poly" coords="121,53,140,47,169,51,186,77,196,80,188,137,156,136,138,97,118,86">
  <area title="Asia" href="https://en.wikipedia.org/wiki/Asia" shape="poly" coords="166,50,184,77,201,74,215,91,258,108,263,87,283,74,297,8,192,3,191,29,187,46,170,42">
  <area title="Australia" href="https://en.wikipedia.org/wiki/Australia_(continent)" shape="poly" coords="257,107,263,85,314,89,316,137,294,151,249,132,248,114">
</map>
```

### `name`

_Defines the name of the map that an image `usemap` attribute will use as value._

`name="world-continents"` : The `<img usemap="#world-continents">` will use this map as overlay.

---

## `mark`

| Type   | Self-closing |
|--------|--------------|
| Inline | ⛔            |

> Defines **highlighted** text.

_Example:_

```html
We use HTML5 to write <mark>content</mark> on the Web.
```

---

## `meta`

| Type | Self-closing |
|------|--------------|
|      | ⛔            |

> Defines **metadata** attached to a web page.

_Example:_

```html
<meta charset="UTF-8">
<meta http-equiv="X-UA-Compatible" content="IE=edge,chrome=1">
<meta name="viewport" content="width=device-width, initial-scale=1">
<meta name="theme-color" content="#ffffff">
```

### `charset`

_Defines the character encoding for the whole web page._

`charset="UTF-8"` : The web page is encoded in UTF-8.

### `http-equiv`

_Defines meta rules for the web page._

`http-equiv="Content-Security-Policy"` : Defines a link to a web page's content policies.

`http-equiv="refresh"` : Allows to refresh the web page every N seconds, or even redirect to another URL.

`http-equiv="X-UA-Compatible"` : Defines which Internet Explorer verison the web page should be rendered as.

### `content`

_Defines the content of the metadata. This varies according to the `name` or `http-equiv` value._

`content="width=device-width, initial-scale=1"` : For the `viewport` metadata, you can specify the width and initial scale of the web page.

`content="2; url=https://site.com"` : For the `refresh` metadata, you can specify how many seconds to wait before redirecting to another URL.

### `name`

_Defines additional information attached to the web page._

`name="viewport"` : Defines dimension and scaling rules for the viewport.

`name="theme-color"` : Defines a theme color which can be used by the browser or the operating system.

---

## `meter`

| Type  | Self-closing |
|-------|--------------|
| Block | ⛔            |

> Defines a **horizontal** meter.

_Example:_

```html
<meter min="0" low="16" value="71" high="92" max="100">Alex</meter><br>
<meter min="0" low="16" value="16" high="92" max="100">Brandon</meter><br>
<meter min="0" low="16" value="40" high="92" max="100">Charlotte</meter><br>
<meter min="0" low="16" value="92" high="92" max="100">Sam</meter><br>
```

### `value`

_Defines the value of the meter, on the scale defined by the **max** attribute.(❗)_

`value="0.7"` : You can use **decimal** and **negative** numbers. It must be between the `min` and `max` values.

`value="-42"` : If you use a value that is lower than the minimum, the meter will be empty.

`value="63"` : If you use a value that is higher than the maximum, the meter will be full.

### `min`

_Defines the **minimum** value possible on the meter._

`min="0"` : Default.

`min="100"` : You can use **decimal** and **negative** numbers.

### `max`

_Defines the **maximum** value possible on the meter._

`max="1"` : Default.

`max="100"` : You can use **decimal** and **negative** numbers.

### `low`

_Defines the lowest value across the range defined by the meter._

`low="0.16"` : The value must be higher than **min** and **lower** than high

### `high`

_Defines the highest value across the range defined by the meter._

`high="0.92"` : The value must be lower than **max** and **higher** than low

---

## `nav`

| Type  | Self-closing |
|-------|--------------|
| Block | ⛔            |

> Defines a section with **navigation links**.

_Example:_

```html
<nav>
    <a href="/">Home</a>
    <a href="/about">About</a>
    <a href="/contact">Contact</a>
  </nav>
```

---

## `noframes`

| Type  | Self-closing |
|-------|--------------|
| Block | ⛔            |

> Defines content displayed when the browser does not support **frames**.

_Example:_

```html
<frameset cols="50%, 50%">
  <frame src="https://site.com/element/frameset">
  <frame src="https://site.com/element/frame">
  <noframes>This browser does not support framesets.</noframes>
</frameset>
```

---

## `noscript`

| Type  | Self-closing |
|-------|--------------|
| Block | ⛔            |

> Defines content displayed when the browser does not have JavaScript enabled. 

_Example:_

```html
<noscript>Please enable JavaScript.</noscript>
```

---

## `ol`

| Type  | Self-closing |
|-------|--------------|
| Block | ⛔            |

> Defines an **ordered list**.

_Example:_

```html
<ol>
  <li>Step one</li>
  <li>Step two</li>
  <li>????</li>
  <li>PROFIT!!!</li>
</ol>
```

### `type`

_Defines how the list is numbered._

`type="1"` : Default.

`type="a"` : Uses lowercase letters.

`type="A"` : Uses uppercase letters.

`type="i"` : Uses lowercase Roman numerals.

`type="I"` : Uses uppercase Roman numerals.

### `start`

_Defines a number to start the list with._

`start="3"` : You can use any **integer**.

### `reversed`

_You can use any integer.(No value required)_

---

## `optgroup`

| Type  | Self-closing |
|-------|--------------|
| Block | ⛔            |

> Defines a group of `<option>` elements.

_Example:_

```html
<select>
  <optgroup label="South America">
    <option>Uruguay</option>
    <option>Brazil</option>
    <option>Argentina</option>
  </optgroup>
  <optgroup label="Europe">
    <option>Italy</option>
    <option>Germany</option>
    <option>England</option>
    <option>France</option>
    <option>Spain</option>
  </optgroup>
</select>
```

### `label`

_Defines the label for the whole group._

`label="South America"` : The label is not selectable.

### `disabled`

_Disables all the options of the group.(No value required)_

---

## `option`

| Type | Self-closing |
|------|--------------|
|      | ⛔            |

> Defines an option within a `<select>` dropdown.

_Example:_

```html
<select name="country">
  <option value="Argentina">Argentina</option>
  <option value="Bolivia">Bolivia</option>
  <option value="Brazil">Brazil</option>
  <option value="Chile">Chile</option>
  <option value="Colombia">Colombia</option>
  <option value="Ecuador">Ecuador</option>
  <option value="Guyana">Guyana</option>
  <option value="Paraguay">Paraguay</option>
  <option value="Peru">Peru</option>
  <option value="Suriname">Suriname</option>
  <option value="Uruguay">Uruguay</option>
  <option value="Venezuela">Venezuela</option>
</select>
```

### `value`

_Defines the `<select>` value if this option is selected.(❗)_

`value="south-africa"` : This value will be sent to the server when the form is submitted.

### `label`

_Defines a label for the option._

`label="Republic of South Africa"` : The label will replace the option inner text.

### `disabled`

_Disables the option.(No value required)_

### `selected`

_Selects the option when the web page loads.(No value required)_

---

## `output`

| Type   | Self-closing |
|--------|--------------|
| Inline | ⛔            |

> Defines the result of a calculation or of **user action**.

_Example:_

```html
<form oninput="sum.value = parseInt(a.value) + parseInt(b.value)">
  <input type="number" name="a" value="4">
  +
  <input type="number" name="b" value="7">
  =
  <output name="sum">11</output>
</form>
```

### `name`

_Defines the unique identifier for that input within the form. It allows the server to access each input's value when submitted._

`name="sum"` : The name value must be unique within the context of a `<form>` container.

---

## `p`

| Type  | Self-closing |
|-------|--------------|
| Block | ⛔            |

> Defines a simple **paragraph** of text. 

_Example:_

```html
<p>Hello World</p>
```

---

## `picture` ⚠️

| Type | Self-closing |
|------|--------------|
|      | ⛔            |

> Defines a container for sources of an `<img>` element.

_Example:_

```html
<picture>
 <source
  media="(min-width: 800px)"
  srcset="/images/sunset-360.jpg 360w,
          /images/sunset-720.jpg 720w,
          /images/sunset-1440.jpg 1440w"
  sizes="33.3vw">
 <source
  srcset="/images/sunset-720.jpg 2x,
          /images/sunset-360.jpg 1x">
 <img src="/images/sunset.jpg" alt="Picture of a Ha Long Bay sunset">
</picture>
```

---

## `pre`

| Type  | Self-closing |
|-------|--------------|
| Block | ⛔            |

> Defines **preformatted** text.

_Example:_

```html
<pre>&lt;!DOCTYPE html&gt;
&lt;html&gt;
  &lt;head&gt;
    &lt;title&gt;Hello World&lt;/title&gt;
  &lt;/head&gt;
  &lt;body&gt;
    &lt;p&gt;Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec viverra nec nulla vitae mollis.&lt;/p&gt;
  &lt;/body&gt;
&lt;/html&gt;</pre>
```

---

## `progress`

| Type  | Self-closing |
|-------|--------------|
| Block | ⛔            |

> Defines a **progress bar**.

_Example:_

```html
<progress value="71" max="100">Alex</progress><br>
<progress value="16" max="100">Brandon</progress><br>
<progress value="40" max="100">Charlotte</progress><br>
<progress value="92" max="100">Sam</progress>
```

### `value`

_Defines the value of the **progress bar**, on the scale defined by the **max** attribute.(❗)_

`value="7"` : You can use **decimal** and **negative** numbers. It must be between the `min` and `max` values.

`value="-42"` : If you use a value that is lower than the minimum, the meter will be empty.

`value="63"` : If you use a value that is higher than the maximum, the meter will be full.

### `max`

_Defines the **maximum** value possible on the meter._

`max="1"` : Default.

`max="100"` : You can use **decimal** and **negative** numbers.

---

## `q`

| Type   | Self-closing |
|--------|--------------|
| Inline | ⛔            |

> Defines a **short quotation**.

_Example:_

```html
He looks around and says <q cite="https://en.wikiquote.org/wiki/The_Terminator">I'll be back</q>.
```

### `cite`

_Defines the source URL of the quotation._

`cite="https://en.wikiquote.org/wiki/The_Terminator"` : You can only use a valid URL.

---

## `rp`

| Type   | Self-closing |
|--------|--------------|
| Inline | ⛔            |

> Defines content displayed when the browser does not support the `<ruby>` element.

_Example:_

```html
<ruby>
  漢 <rp>(</rp><rt>Kan</rt><rp>)</rp>
  字 <rp>(</rp><rt>ji</rt><rp>)</rp>
</ruby>
```

---

## `rt`

| Type   | Self-closing |
|--------|--------------|
| Inline | ⛔            |

> Defines the pronunciation of ruby annotations.

_Example:_

```html
<ruby>
  漢 <rp>(</rp><rt>Kan</rt><rp>)</rp>
  字 <rp>(</rp><rt>ji</rt><rp>)</rp>
</ruby>
```

---

## `rtc`

| Type   | Self-closing |
|--------|--------------|
| Inline | ⛔            |

> Defines a text container within ruby annotations.

_Example:_

```html
<ruby>
   <rb>旧</rb>
   <rb>金</rb>
   <rb>山</rb>
   <rt>jiù</rt>
   <rt>jīn</rt>
   <rt>shān</rt>
   <rtc>San Francisco</rtc>
</ruby>
```

--- 

## `ruby`

| Type   | Self-closing |
|--------|--------------|
| Inline | ⛔            |

> Defines a ruby annotation to show the pronunciation of East Asian characters.

_Example:_

```html
<ruby>
  漢 <rp>(</rp><rt>Kan</rt><rp>)</rp>
  字 <rp>(</rp><rt>ji</rt><rp>)</rp>
</ruby>
```

---

## `s`

| Type   | Self-closing |
|--------|--------------|
| Inline | ⛔            |

> Defines strikethrough text.

_Example:_

```html
Alex is <s>37</s> 38 years old.
```

---

## `samp`

| Type   | Self-closing |
|--------|--------------|
| Inline | ⛔            |

> Defines a sample output from a computer program.

_Example:_

```html
I entered <code>git push</code> and the terminal printed out <samp>Everything up-to-date</samp>.
```

---

## `script`

| Type | Self-closing |
|------|--------------|
|      | ⛔            |

> Defines a container for an external script.

_Example:_

```html
<script src="https://site.com/javascript/my-scripts.js"></script>
```

### `src`

_Defines the source of the external script._

`src="https://site.com/javascript/my-scripts.js"` : Defines the source of the external script.

### `type`

_Defines the MIME type of the external script._

`type="text/javascript"` : This is for .js files.

### `async`

_Allows the external script to be loaded asynchronously.(No value required.)_

---

## `section`

| Type  | Self-closing |
|-------|--------------|
| Block | ⛔            |

> Defines a **section** within a web page.

_Example:_

```html
<section>
  <h2>Section title</h2>
  <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec viverra nec nulla vitae mollis.</p>
</section>
```

---

## `select`

| Type  | Self-closing |
|-------|--------------|
| Block | ⛔            |

> Defines a select dropdown with different `<option>` elements.

_Example:_

```html
<select name="country">
  <option value="Argentina">Argentina</option>
  <option value="Bolivia">Bolivia</option>
  <option value="Brazil">Brazil</option>
  <option value="Chile">Chile</option>
  <option value="Colombia">Colombia</option>
  <option value="Ecuador">Ecuador</option>
  <option value="Guyana">Guyana</option>
  <option value="Paraguay">Paraguay</option>
  <option value="Peru">Peru</option>
  <option value="Suriname">Suriname</option>
  <option value="Uruguay">Uruguay</option>
  <option value="Venezuela">Venezuela</option>
</select>
```

### `name`

_Defines the unique identifier for that select within the form.(❗)_

`name="country"` : The name value must be unique within the context of a `<form>` container.

### `size`

_When `multiple` is present too, defines the height of the select list._

`size="5"` : You can use any **integer** value.

### `multiple`

_Allows to select multiple options at once.(No value required.)_

### `disabled`

_Disables the button(No value required.)_

### `autofocus`

_Sets focus on the select when the web page loads.(No value required.)_

### `required`

_Sets focus on the select when the web page loads.(No value required.)_

---

## `small`

| Type   | Self-closing |
|--------|--------------|
| Inline | ⛔            |

> Defines small print, for less important content. 

_Example:_

```html 
<p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec viverra nec nulla vitae mollis.</p>
<small>Posted on <time datetime="2017-04-29T19:00">Apr 29</time> in <a href="/category/code">Code</a></small>
```

---

## `source`

| Type | Self-closing |
|------|--------------|
|      | ✅            |

> Defines a source for an `<audio>`, `<video>`, or `<picture>` element.

_Example:_

```html
<picture>
 <source
  media="(min-width: 800px)"
  srcset="/images/sunset-360.jpg 360w,
          /images/sunset-720.jpg 720w,
          /images/sunset-1440.jpg 1440w"
  sizes="33.3vw">
 <source
  srcset="/images/sunset-720.jpg 2x,
          /images/sunset-360.jpg 1x">
 <img src="/images/sunset.jpg" alt="Picture of a Ha Long Bay sunset">
</picture>
```

### `src`

### `src`

_The URL where the image is hosted.(❗)_

`src="/images/tiramisu.jpg"` : You can use a **relative** URL.

`src="https://site.com/images/traffic.jpg"` : You can use an **absolute** URL.

### `srcset`

_Defines a list of different **sources** for the same image. The browser will choose the best one to use._

`srcset="/images/sunset-@2x.jpg 2x"` : You can define a pixel density descriptor like `2x`. In this case, `sunset-@2x.jpg` is `720px` wide.

`srcset="/images/sunset-360.jpg 360w` : You can use a **width descriptor** like `360w`. This value is divided by one of the source sizes (defined in the sizes attribute) to obtain the **pixel density**.

### `sizes`

_Defines a list of different source **sizes**. You can combine each of them with a **media query**._

`sizes="(min-width: 800px) 1440px, 720px"` : The browser will use the `1440px` image (defined in srcset) if the viewport is larger than `800px`.
It will use the `720px` otherwise.

### `type`

_Defines the MIME type of the source._

`type="image/jpeg"` : This is for `.jpg` files.

### `media`

_Defines a media query for a `<picture>` source._

`media="(min-width: 800px)"` : The media will only be used on viewports larger than 800px.

---

## `span`

| Type   | Self-closing |
|--------|--------------|
| Inline | ⛔            |

> Defines a **generic** inline container of content, that does not carry any semantic value.

_Example:_

```html
Lorem ipsum<span> dolor sit amet, consectetur adipiscing elit</span>. Donec viverra nec nulla vitae mollis.
```

---

## `strong`

| Type   | Self-closing |
|--------|--------------|
| Inline | ⛔            |

> Defines **strong importance** on text.

_Example:_

```html
HTML should only be used to write <strong>content</strong>, and keep CSS for <strong>styling</strong> the web page.
```

---

## `style`

| Type   | Self-closing |
|--------|--------------|
| Inline | ⛔            |

>Defines a container to add **CSS** within a web page.

_Example:_

```html
<style type="text/css">
  .important {
    color: red;
  }
</style>
<p class="important">Lorem ipsum dolor sit amet, consectetur adipiscing elit.</p>
```

### `type`

_Defines the MIME type of the style block._

`type="text/css"` : This is for `.css` content.

---

## `sub`

| Type   | Self-closing |
|--------|--------------|
| Inline | ⛔            |

> Defines text that should be displayed **lower**.

_Example:_

```html
The formula of carbon dioxide is CO<sub>2</sub>.
```

---

## `summary`

| Type   | Self-closing |
|--------|--------------|
| Inline | ⛔            |

> Defines the summary of a `<details>` element.

_Example:_

```html
<details>
  <summary>Read more</summary>
  <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec viverra nec nulla vitae mollis.</p>
</details>
```

---

## `sup`

| Type   | Self-closing |
|--------|--------------|
| Inline | ⛔            |

> Defines text that should be displayed **higher**. 

_Example:_

```html
The "power of two" is 2<sup>n</sup> where n is an integer.
```

---

## `table`

| Type  | Self-closing |
|-------|--------------|
| Block | ⛔            |

> Defines a container for **tabular data**.

_Example:_

```html
<table>
  <thead>
    <tr>
      <th>Name</th>
      <th>Instrument</th>
    </tr>
  </thead>
  <tfoot>
    <tr>
      <th>Name</th>
      <th>Instrument</th>
    </tr>
  </tfoot>
  <tbody>
    <tr>
      <td>John Lennon</td>
      <td>Rhythm Guitar</td>
    </tr>
    <tr>
      <td>Paul McCartney</td>
      <td>Bass</td>
    </tr>
    <tr>
      <td>George Harrison</td>
      <td>Lead Guitar</td>
    </tr>
    <tr>
      <td>Ringo Starr</td>
      <td>Drums</td>
    </tr>
  </tbody>
</table>
```

---

## `tbody`

| Type  | Self-closing |
|-------|--------------|
| Block | ⛔            |

> Defines a group of table rows `<tr>`.

_Example:_

```html
<table>
  <thead>
    <tr>
      <th>Name</th>
      <th>Instrument</th>
    </tr>
  </thead>
  <tfoot>
    <tr>
      <th>Name</th>
      <th>Instrument</th>
    </tr>
  </tfoot>
  <tbody>
    <tr>
      <td>John Lennon</td>
      <td>Rhythm Guitar</td>
    </tr>
    <tr>
      <td>Paul McCartney</td>
      <td>Bass</td>
    </tr>
    <tr>
      <td>George Harrison</td>
      <td>Lead Guitar</td>
    </tr>
    <tr>
      <td>Ringo Starr</td>
      <td>Drums</td>
    </tr>
  </tbody>
</table>
```

---

## `td`

| Type | Self-closing |
|------|--------------|
|      | ⛔            |

> Defines a table cell. Must be a direct child of a `<tr>`.

_Example:_

```html
<table>
  <thead>
    <tr>
      <th colspan="4">World Cup winners</th>
    </tr>
    <tr>
      <td colspan="2">Location</td>
      <td colspan="2">Score</td>
    </tr>
    <tr>
      <td>Continent</td>
      <td>Country</td>
      <td>First</td>
      <td>Total</td>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td rowspan="3">South America</td>
      <td>Uruguay</td>
      <td>1930</td>
      <td>2</td>
    </tr>
    <tr>
      <td>Brazil</td>
      <td>1958</td>
      <td>5</td>
    </tr>
    <tr>
      <td>Argentina</td>
      <td>1978</td>
      <td>2</td>
    </tr>
    <tr>
      <td rowspan="5">Europe</td>
      <td>Italy</td>
      <td>1934</td>
      <td>4</td>
    </tr>
    <tr>
      <td>Germany</td>
      <td>1954</td>
      <td>4</td>
    </tr>
    <tr>
      <td>England</td>
      <td>1966</td>
      <td>1</td>
    </tr>
    <tr>
      <td>France</td>
      <td>1998</td>
      <td>1</td>
    </tr>
    <tr>
      <td>Spain</td>
      <td>2010</td>
      <td>1</td>
    </tr>
  </tbody>
</table>
```

### `colspan`

_Defines how many columns a cell should span across._

`colspan="3"` : You can use any integer.

### `rowspan`

_Defines how many columns a cell should span across._

`rowspan="3"` : You can use any integer.

---

## `template` ⚠️

| Type  | Self-closing |
|-------|--------------|
| Block | ⛔            |

> Defines a placeholder for content that can be displayed using JavaScript.

---

## `textarea`

| Type   | Self-closing |
|--------|--------------|
| Inline | ⛔            |

> Defines a multi-line text control within a web form.

### `name`

_Defines the unique identifier for that textarea within the form. It allows the server to access each textarea's value when submitted.(❗)_

`name="message"` : The name value must be unique within the context of a `<form>` container.

### `autocomplete`

_Determines if the browser can autocomplete the textarea._

`autocomplete="on"` : The browser will **enable** autocomplete functions.

`autocomplete="off"` : The browser will **disable** autocomplete functions.

### `minlength`

_Defines the minimum amount of characters the textarea required to be valid._

`minlength="10"` : You can use **integers**.

### `maxlength`

_Defines the maximum amount of characters the textarea can contain._

`maxlength="100"` : You can use **integers**.

### `placeholder`

_Defines a non-selectable placeholder text that only appears when the textarea is empty._

`placeholder="Enter your message here"` : You can hint at the format expected for the textarea.

### `rows`

_Defines the number of rows._

`rows="5"` : You can use **integers**.

### `cols`

_Defines the number of columns._

`cols="50"` : You can use **integers**.

### `wrap`

_Defines how the text should be wrapped._

`wrap="hard"` : The text will always be wrapped depending on the `cols` value.

`wrap="soft"` : The text will only break when needed.

### `disabled`

_Disables the textarea.(No value required.)_

### `readonly`

_Turns the textarea into a read-only element.(No value required.)_

### `required`

_Tells the browser that this textarea is **required**. Leaving it empty will show a warning.(No value required.)_

### `autofocus`

_Sets focus on the textarea when the web page loads.(No value required.)_

### `spellcheck`

_Enables the browser spell checker.(No value required.)_

---

## `tfoot`

| Type  | Self-closing |
|-------|--------------|
| Block | ⛔            |

> Defines a group of table rows `<tr>` at the end of a `<table>`.

_Example:_

```html
<table>
  <thead>
    <tr>
      <th>Name</th>
      <th>Instrument</th>
    </tr>
  </thead>
  <tfoot>
    <tr>
      <th>Name</th>
      <th>Instrument</th>
    </tr>
  </tfoot>
  <tbody>
    <tr>
      <td>John Lennon</td>
      <td>Rhythm Guitar</td>
    </tr>
    <tr>
      <td>Paul McCartney</td>
      <td>Bass</td>
    </tr>
    <tr>
      <td>George Harrison</td>
      <td>Lead Guitar</td>
    </tr>
    <tr>
      <td>Ringo Starr</td>
      <td>Drums</td>
    </tr>
  </tbody>
</table>
```

---

## `th`

| Type | Self-closing |
|------|--------------|
|      | ⛔            |

> Defines a table header. Must be a direct child of a `<tr>`.

_Example:_

```html
<table>
  <thead>
    <tr>
      <th colspan="4">World Cup winners</th>
    </tr>
    <tr>
      <td colspan="2">Location</td>
      <td colspan="2">Score</td>
    </tr>
    <tr>
      <td>Continent</td>
      <td>Country</td>
      <td>First</td>
      <td>Total</td>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td rowspan="3">South America</td>
      <td>Uruguay</td>
      <td>1930</td>
      <td>2</td>
    </tr>
    <tr>
      <td>Brazil</td>
      <td>1958</td>
      <td>5</td>
    </tr>
    <tr>
      <td>Argentina</td>
      <td>1978</td>
      <td>2</td>
    </tr>
    <tr>
      <td rowspan="5">Europe</td>
      <td>Italy</td>
      <td>1934</td>
      <td>4</td>
    </tr>
    <tr>
      <td>Germany</td>
      <td>1954</td>
      <td>4</td>
    </tr>
    <tr>
      <td>England</td>
      <td>1966</td>
      <td>1</td>
    </tr>
    <tr>
      <td>France</td>
      <td>1998</td>
      <td>1</td>
    </tr>
    <tr>
      <td>Spain</td>
      <td>2010</td>
      <td>1</td>
    </tr>
  </tbody>
</table>
```

### `colspan`

_Defines how many columns a cell should span across._

`colspan="3"` : You can use any integer.

### `rowspan`

_Defines how many columns a cell should span across._

`rowspan="3"` : You can use any integer.

---

## `thead`

| Type  | Self-closing |
|-------|--------------|
| Block | ⛔            |

> Defines a group of table rows `<tr>` at the start of a `<table>`.

_Example:_

```html
<table>
  <thead>
    <tr>
      <th>Name</th>
      <th>Instrument</th>
    </tr>
  </thead>
  <tfoot>
    <tr>
      <th>Name</th>
      <th>Instrument</th>
    </tr>
  </tfoot>
  <tbody>
    <tr>
      <td>John Lennon</td>
      <td>Rhythm Guitar</td>
    </tr>
    <tr>
      <td>Paul McCartney</td>
      <td>Bass</td>
    </tr>
    <tr>
      <td>George Harrison</td>
      <td>Lead Guitar</td>
    </tr>
    <tr>
      <td>Ringo Starr</td>
      <td>Drums</td>
    </tr>
  </tbody>
</table>
```

---

## `time`

| Type   | Self-closing |
|--------|--------------|
| Inline | ⛔            |

> Defines a time on a 24h clock.

_Example:_

```html
The game starts at <time datetime="2017-04-29T19:00">19:00</time>.
```

### `datetime`

_Defines when the deletion has occurred._

`datettime="2017-04-29T19:00"` : You need a valid datettime string.

---

## `title`

| Type | Self-closing |
|------|--------------|
|      | ⛔            |

> Defines the **title** of the web page, displayed on the browser tab.

_Example:_

```html
<title>The title element</title>
```

---

## `tr`

| Type | Self-closing |
|------|--------------|
|      | ⛔            |

> Defines a table row.

_Example:_

```html
<table>
  <thead>
    <tr>
      <th colspan="4">World Cup winners</th>
    </tr>
    <tr>
      <td colspan="2">Location</td>
      <td colspan="2">Score</td>
    </tr>
    <tr>
      <td>Continent</td>
      <td>Country</td>
      <td>First</td>
      <td>Total</td>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td rowspan="3">South America</td>
      <td>Uruguay</td>
      <td>1930</td>
      <td>2</td>
    </tr>
    <tr>
      <td>Brazil</td>
      <td>1958</td>
      <td>5</td>
    </tr>
    <tr>
      <td>Argentina</td>
      <td>1978</td>
      <td>2</td>
    </tr>
    <tr>
      <td rowspan="5">Europe</td>
      <td>Italy</td>
      <td>1934</td>
      <td>4</td>
    </tr>
    <tr>
      <td>Germany</td>
      <td>1954</td>
      <td>4</td>
    </tr>
    <tr>
      <td>England</td>
      <td>1966</td>
      <td>1</td>
    </tr>
    <tr>
      <td>France</td>
      <td>1998</td>
      <td>1</td>
    </tr>
    <tr>
      <td>Spain</td>
      <td>2010</td>
      <td>1</td>
    </tr>
  </tbody>
</table>
```

---

## `track`

| Type | Self-closing |
|------|--------------|
|      | ✅            |

> Defines text tracks (like subtitles) for` <audio>` and `<video>` elements.

---

## `u`

| Type   | Self-closing | 
|--------|--------------|
| Inline | ⛔            |

> Makes an element's text **underlined**.

_Example:_

```html
Hello <u>World</u>!
```

---

## `ul`

| Type  | Self-closing | 
|-------|--------------|
| Block | ⛔            |

> Defines an **unordered list**. 

_Example:_

```html
<p>My shopping list:</p>
<ul>
  <li>Milk</li>
  <li>Bread</li>
  <li>Chocolate</li>
  <li>More chocolate</li>
</ul>
```

---

## `var`

| Type  | Self-closing | 
|-------|--------------|
| Block | ⛔            |

> Defines a **variable** in a mathematical or programming expression.

_Example:_

```html
The value of <var>x</var> is 12.
```

---

## `wbr` ⚠️

| Type  | Self-closing | 
|-------|--------------|
| Block | ⛔            |

> Defines a location within a block of text where the browser could eventually insert **line break**.