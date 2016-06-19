## Three broad categories of body markup
**Structural** - Defines document and layout structure
**Stylistic** - Modifies the appearance of text
**Semantic** - Identifies specific types of information

## Structural Markup
``` HTML
Headings: <h1>, <h2>, <h3>, <h4>, <h5>, <h6> 
Paragraphs: <p>
Lists: <dl>, <ol>, <ul> 
Block and inline content: <div> and <span>
```
## Stylistic Markup
``` HTML
Bold: <em>, <strong> 
Deleted: <del>
Italic: <i> 
Preformatted: <pre>
Subscript: <sub> 
Superscript: <sup>
``` 
## Semantic Markup
``` HTML
Links: <a> 
Tables: <table>
Forms: <form> 
Images: <img>
Others: <address>, <code>
```
<br />

---

## Block-level and inline elements
* By default, block-level elements begin on newlines whereas inline elements do not 
* Block-level elements may contain inline elements and other block-level elements 
* Inline elements may contain only data and other inline elements
<br />

---

## Anchor
* Provides a one-way link from one document to another
<br />

---

## Uniform Resource Locator (URL)
A formal representation of the location and means of access for a resource on the Internet.
> e.g.
```
scheme://user:password@host:port/path?query#fragment
http://www.example.com/index.html
http://www.example.com/path/to/image.jpg
http://www.example.com/search? query=cats&sortby=cuteness
http://www.example.com/page.html#section1
```

<br />

---

## Absolute VS. Relative URLs
**Absolute** URL to a file in the **top** level directory
> e.g.
```
http://www.example.com/page.html 
/page.html
```

**Absolute** URL to a file in a **subdirectory**
> e.g.
```
http://www.example.com/subdir/page.html 
/subdir/page.html
```

<br />
**Relative** URL to a file in the **current** directory
> e.g.
```
page.html 
./page.html
```

**Relative** URL to a file in a **subdirectory** of the **current** directory
> e.g.
```
subdir/page.html
subdir/subdir2/page.html
```

**Relative** URL to a file in the **parent** directory
> e.g.
```
../page.html 
../../page.html
```

<br />

---
## HTML Escapes
You must always escape
```
Less than (<) - &lt; 
Greater than (>) - &gt;
Ampersand (&) - &amp;
```

<br />

---
## Forms
``` HTML
<form action="http://localhost/cgi-bin/env.py" method="post"> 
    <input type="text" name="foo" /> 
    <input type="submit" /> 
</form>
```

### Form Attributes
* Action is the URL of a program that processes the form input
* Method must be one of POST or GET
    * An idempotent request is one that does not produce "side effects".
    * GET requests are expected to be idempotent whereas POST requests are expected to produce side effects

<br />

---

## Input controls
* text input boxes (single line and multi-line) 
* checkboxes 
* radio buttons 
* submit, reset buttons 
* buttons (other than submit and reset) 
* hidden fields

<br />
* A single HTML document can contain multiple forms, and hence multiple submit buttons. 
* However, forms cannot be nested. That is, one form cannot be inside another. 
* It is possible to write the CGI script to produce a form as output, and also act as the recipient of the form data (by being the "action” of the form).

<br />

---
## Some extra things
* Accessibility - Using descriptive tags to aid screen-readers and audio browsers 
* Search-engine optimisation (SEO) - Bumping your site to the top of the Google listing ... 
* "Semantic web" - All about having descriptive tags in everything so that it can be more efficiently mined. controversial idea ...