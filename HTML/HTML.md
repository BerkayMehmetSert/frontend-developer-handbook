<h1 align="center">HTML GUIDE</h1>

> _Free guide to HTML. It features all elements and attributes._

**Guideline:**

> * ✅ : Yes
> * ⛔ : No
> * ❗  : Required
> * ⚠️ : Experimental




## `a` 

| Type   | Self-closing | 
|--------|--------------|
| Inline | ⛔            |

> Creates a **link** to a URL: a web page, a section within a page, an email address... Also called the `anchor` element, where the `a` comes from.

_Example:_

```html
<a href="https://site.com">HTML Reference</a>
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

## `dialog`

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