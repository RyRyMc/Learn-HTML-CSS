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
