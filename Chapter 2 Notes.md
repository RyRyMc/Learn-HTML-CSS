# *Notes* Chapter 2: Getting to Know HTML

## Semantics Overview
HTML Semantics is the practice of giving content on the page meaning and structure by using the proper element.

## Identifying Divisions & Spans
\<div>s and \<span>s are used for styling.

They allow you to target contained sets of content by placing a *class* or *id* attribute in them.

### Block vs. Inline Elements
* ***Block-level*** elements begin on a new line, stack up on top of each other, and occupy any available width.
* ***Inline-level*** elements do not begin on a new line, line up one after the other, and maintain the width of their content.

\<div> is a ***block-level*** element.

\<span> is a ***inline-level*** element.

[Shay Howe](https://learn.shayhowe.com/html-css/getting-to-know-html/) gave a great example here:
>For example, if we have a \<div> with an orange background that contains social media links, our first thought might be to give the \<div>
>a class value of orange. What happens if that orange background is later changed to blue? Having a class value of orange no longer makes
>sense. A more sensible choice for a class value would be social, as it pertains to the contents of the \<div>, not the style.

#### HTML
```html
<div class="social">
  <p>I may be found on...</p>
  <p>Additionally, I have a profile on...</p>
</div>

<!-- Span -->
<p>Soon we'll be <span class="tooltip">writing HTML</span> with the best of them.</p>
```

### Comments within HTML & CSS
* Comments can be added in HTML with \<!-- at the beginning and a \--> at the end.
* Comments can be added in CSS with /\* at the beginning and a \*/ at the end.

## Using Text-Based Elements

### Headings
Headings are a ***block-level*** element.

Headings establish the hierarchy of the content on the page.

Example of headers:
#### HTML
```html
<h1>Heading Level 1</h1>
<h2>Heading Level 2</h2>
<h3>Heading Level 3</h3>
<h4>Heading Level 4</h4>
<h5>Heading Level 5</h5>
<h6>Heading Level 6</h6>
```
#### Results
> <h1>Heading Level 1</h1>
> <h2>Heading Level 2</h2>
> <h3>Heading Level 3</h3>
> <h4>Heading Level 4</h4>
> <h5>Heading Level 5</h5>
> <h6>Heading Level 6</h6>

### Paragraphs
Paragraphs usually follow heading to provide supporting info.

Example of paragraphs:
#### HTML
```html
<p>Steve Jobs was a co-founder and longtime chief executive officer at Apple. On June 12, 2005, Steve gave the commencement address at Stanford University.</p>

<p>In his address Steve urged graduates to follow their dreams and, despite any setbacks, to never give up&ndash;advice which he sincerely took to heart.</p>
```
#### Results
> <p>Steve Jobs was a co-founder and longtime chief executive officer at Apple. On June 12, 2005, Steve gave the commencement address at Stanford University.</p>

> <p>In his address Steve urged graduates to follow their dreams and, despite any setbacks, to never give up&ndash;advice which he sincerely took to heart.</p>

### Bold Text with Strong
There are two ways to bold text in HTML: \<strong> and \<b>

* ***\<strong>*** is an element that semantically means *"strong importance"*
* ***\<b>*** is an element that semantically means *“stylistically offset” text"*

Example of using both:

#### HTML
```html
<!-- Strong importance -->
<p><strong>Caution:</strong> Falling rocks.</p>

<!-- Stylistically offset -->
<p>This recipe calls for <b>bacon</b> and <b>baconnaise</b>.</p>
```

#### Results
> <p><strong>Caution:</strong> Falling rocks.</p>

> <p>This recipe calls for <b>bacon</b> and <b>baconnaise</b>.</p>

### Italicize Text with Emphasis
There are two ways to italicize text in HTML:

* ***\<em>*** is an element that semantically means *"stress emphasis"*.
* ***\<i>*** is an element that semantically means *"strong importance"*

Example of using both:

#### HTML
```html
<!-- Stressed emphasis -->
<p>I <em>love</em> Chicago!</p>

<!-- Alternative voice or tone -->
<p>The name <i>Shay</i> means a gift.</p>
```

#### Results
> <p>I <em>love</em> Tulsa!</p>

> <p>The name <i>Ryan</i> means little king.</p>

## Building Structure
HTML5 includes structurally based elements that give intentionality to the sections of a website.

### Header
The \<header> element is used to identify the top of a page, article, section, or segment of a page.

#### HTML
```html
<header>...</header>
```

### Navigation
The \<nav> element identifies a section of major navigational links.

#### HTML
```html
<nav>...</nav>
```

### Article
The \<article> element is used to identify a section of independent, self-contained content that may be independently distributed or reused.

#### HTML
```html
<article>...</article>
```

### Section
The \<section> element is used to identify a thematic grouping of content, which generally, but not always, includes a heading.

#### HTML
```html
<section>...</section>
```

### Aside
The \<aside> element holds content, such as sidebars, inserts, or brief explanations, that is tangentially related to the content surrounding it.

#### HTML
```html
<aside>...</aside>
```

### Footer
The \<footer> identifies the closing or end of a page, article, section, or other segment  of a page.

#### HTML
```html
<footer>...</footer>
```

## Creating Hyperlinks
Hyperlinks provide the ability to link from one web page or resource to another. 

Hyperlinks are established using the \<a> anchor tag, which is an inline element, and an href attribute.

Example of hyperlink:

#### HTML
```html
<a href="http://ryanmccall.com">Ryan</a>
```

#### Results
> <a href="http://rya.com">Ryan</a>

### Relative and Absolute Paths
Links have two common types: *relative* path and *absolute* path

* ***Relative*** path links point to other pages on the same website.
  * omit the domain (.com, .org, .edu) in the href
* ***Absolute*** path links point to other websites
  * include the full href (http://google.com)

Example of Hyperlinks:

#### HTML
```html
<!-- Relative Path -->
<a href="about.html">About</a>

<!-- Absolute Path -->
<a href="http://www.google.com/">Google</a>
```

#### Results
> <!-- Relative Path -->
> <a href="about.html">About</a>

> <!-- Absolute Path -->
> <a href="http://www.google.com/">Google</a>

### Linking to an Email Address
Creating a hyperlink that links to an email is easy as adjusting the href

* Add *mailto:* followed my the email address to automatically open the user email service of choice with you email automatically generated to the *To:* section
* Follow the email address with *?* to add specific information to the email and separate them with *&*
  * *subject=* to auto-generate the subject of the email
    * Separate each word with %20
  * *body=* to auto-generate the body of the email
    * Separate each word with %20
    
Example of email hyperlink:

#### HTML
```html
<a href="mailto:ryan@awesome.com?subject=Reaching%20Out&body=How%20are%20you">Email Me</a>
```

#### Results
> <a href="mailto:shay@awesome.com?subject=Reaching%20Out&body=How%20are%20you">Email Me</a>

### Opening Links in a New Window
Creating a link that opens in another window takes one addition to the link.

* Add a *target=* attributte and setting it to *"_blank"*

Example of a link that opens in a new window:

#### HTML
```html
<a href="http://ryanmccall.com/" target="_blank">Ryan McCall</a>
```

#### Results
> <a href="http://ryanmccall.com/" target="_blank">Ryan McCall</a>

### Linking to Parts of the Same Page
Creating a link to a part of the same page takes two steps

* Add an *id* attribute to the element you wish to link to on the page
* link the href to the id with a #

Example of linking to parts of the same page:

#### HTML
```html
<body id="top">
  ...
  <a href="#top">Back to top</a>
  ...
</body>
```

#### Results
<body id="top">
  ...
  <a href="#top">Back to top</a>
  ...
</body>
