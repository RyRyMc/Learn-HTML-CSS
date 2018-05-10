# *Notes* Chapter 1: Building Your First Web Page

* [What is HTML & CSS?](#what-is-html---css-)
* [Understanding Common HTML Terms](#understanding-common-html-terms)
	* [Elements](#elements)
	* [Tags](#tags)
	* [Attributes](#attributes)
* [Setting Up the HTML Document Structure](#setting-up-the-html-document-structure)
* [Understanding Common CSS Terms](#understanding-common-css-terms)
	* [Selectors](#selectors)
	* [Properties](#properties)
	* [Values](#values)
* [Working with Selectors](#working-with-selectors)
	* [Type Selectors](#type-selectors)
	* [Class Selectors](#class-selectors)
	* [ID Selectors](#id-selectors)
* [Referencing CSS](#referencing-css)
* [Using CSS Resets](#using-css-resets)

## What is HTML & CSS?
HTML stands for HyperText Markup Language. This language is used to provide the structure of the webpage.

CSS stands for Cascading Style Sheets. This language is used to change the appearance of the webpage.

## Understanding Common HTML Terms

### Elements
Elements are designators that define the structure of the page. 

Examples of elements are:

* h1 thru h6 *Headers*
* p *Paragraphs*

### Tags
By placeing a \<> around an element, you create a tag.

There are two types of tags: **opening** and **closing**

* Opening tags are defined by a element placed inside of \<> like \<p>.
* Closing tags look much like opening tags by include a / before the element like \</p>

Tags help define how the content inbetween them is to be displayed.

### Attributes
Attributes appear inside the opening tag after the element. They are used to provide additional information about the element.

## Setting Up the HTML Document Structure
HTML documents are saved in a file ending in **.html** and follow the same structure.

#### HTML
```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8">
    <title>Hello World</title>
  </head>
  <body>
    <h1>Hello World</h1>
    <p>This is a web page.</p>
  </body>
</html>
```

## Understanding Common CSS Terms

### Selectors
Selectors are used to designate which HTML element or elements are being targeted by the CSS for styling.

Selectors are placed before the curly braces in a CSS statement.

Examples of selectors are:
* Any element (h1 thru h6, p...).
* An attribute like *id* or *class*.

#### CSS
```css
p { ... }
```

### Properties
Properties are used to specify part of an element to style.

Example properties are:
* background
* color
* font-size
* height
* width

#### CSS
```css
p {
color: ...;
font-size: ...;
}
```

### Values
Values are used to define the style of the property that has been selected.

Values are placed after a property between a colon and a semicolon.

#### CSS
```css
p {
  color: orange;
  font-size: 16px;
}
```

## Working with Selectors

### Type Selectors
Type selectors target a specific HTML element for styling.

#### HTML
```html
<div>...</div>
<div>...</div>
```

#### CSS
```css
div {
	...
}
```

### Class Selectors
Class selectors target the class attribute of an element for styling.

This means that if different elements have the same class attribute, they receive the same styling.

Class selectors look slightly different to Type selectors because they have a . placed before there name.

#### HTML
```html
<div class="awesome">...</div>
<p class="awesome">...</p>
```

#### CSS
```css
.awesome {
	...
}
```

### ID Selectors
ID selectors target a single element's id attribute.

ID selectors are unique from type and class because they have a # placed before there name.

#### HTML
```html
<div id="ryanmccall">...</div>
```

#### CSS
```css
#ryanmccall {
	...
}
```

## Referencing CSS
For the HTML document to know that the CSS document exists, we must reference it in the HTML \<head>.

The CSS file will be saved with a file ending of **.css**.

A \<link> is created in \<head> of the HTML with two attributes: *rel* and *href*.
* *rel* tells the HTML document what the relationship is between the HTML document and linked document.
* *href* tells the HTML document where to find the linked document. 
	* If the document is not in the same folder as the HTML, make sure to show the path to the correct location.

#### HTML
```html
<head>
  <link rel="stylesheet" href="main.css">
</head>
```

## Using CSS Resets
So that it is easier to style your HTML, adding a reset to the top of the CSS will help you to be able to style everything from fresh slate.

A popular one is http://meyerweb.com/eric/tools/css/reset/
