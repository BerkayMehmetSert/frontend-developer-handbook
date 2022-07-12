<h1 align="center">NAMING & PATHS CHEAT SHEET</h1>

**Table of content**

- [Naming conventions](#Naming-conventions)
- [Paths-folders](#Paths-folders)

---

## Naming conventions

### `all lowercase`

- All files & folder must us only lowercase characters.

- This includes extensions, like `.jpg`, `.png`,` etc`.

- The only exceptions are `README.md`, `LICENSE` & `CNAME`.

_Good examples:_

`index.html` — all lowercase.

`t-rex.png` — no spaces, dashes separating words.

`dragon-1.jpg` — only letters, numbers & dashes.

### `Nospaces`

* No spaces allowed anywhere in file & folder names.

* Be careful their are spaces hidden at the end, after the extension.

* Use a dash (`-`) to separate words.

_Bad examples:_

`Index.html` — capital letters used.

`t rex.png` — space in filename.

`dragon’s egg.jpg` — apostrophe is a non-standard character.

### `Only letters, numbers & dashes`

* Use dashes (`-`) to separate words, e.g. super-duper.html.

* The only exception is the dot (`.`) before extensions.

* Underscores (`_`) are also acceptable.

_Be careful:_

`dragon.JPG` — some programs like to use uppercase extensions—change them to lowercase.

`full-site.tar.gz` — multiple extensions are okay.

`_archive` — underscores are fine, but try to avoid them.

## Paths-folders

### `./` or nothing

Start in the same location.

`./about.html` or `about.html`

### `../`

Go out of a folder.

Can be chained: `../../`.

`../index.html`

### `//`

Start immediately after the protocol, replace the domain.

`//github.com`

### `https://`

Start at the top level of the Internet, replace everything.

`https://github.com`

### `/`

Start at the root of the computer or the root of the domain.

`/index.html` or `/Dropbox/image.jpg`

### `~/`

Start in your home folder.

> ⚠️ Doesn’t work on the web.

`~/Desktop/todo.txt`

