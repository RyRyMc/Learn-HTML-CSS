# ***Notes*** Chapter 3: Getting to Know CSS

## The Cascade

Within CSS, all styles cascade from the top of a sheet to the bottom.

[Shay Howe](https://learn.shayhowe.com/html-css/getting-to-know-css/) gave a good explanation of this:

> For example, say we select all paragraph elements at the top of our style sheet and set their background color to orange and their font size to 24 pixels. Then towards the bottom of our style sheet, we select all paragraph elements again and set their background color to green, as seen here.

#### CSS
```css
p {
  background: orange;
  font-size: 24px;
}
p {
  background: green;
}
```

> Because the paragraph selector that sets the background color to green comes after the paragraph selector that sets the background color to orange, it will take precedence in the cascade. All of the paragraphs will appear with a green background. The font size will remain 24 pixels because the second paragraph selector didn’t identify a new font size.

### Cascading Properties
This also works inside of individual selectors.

#### CSS
```css
p {
  background: orange;
  background: green;
}
```

The background will be green because it was the the last style give for background.

## Calculating Specificity
Each of the CSS selectors have a different weight that will determine when they will render.

* The type selector has the lowest specificity weight, which is 0-0-1.
* The class selector has a medium specificity weight, which is 0-1-0.
* The id slector has a high specificity, which is 1-0-0.

So, if an element is selcted by a type and an id, the id will out weight the type

## Combining Selectors
When selectors are combined they should be read right to left where the closest selector to the curly braces is referred to as the key selector and any selctor to the left of the key selector is a prequalifier.

#### HTML
```html
<div class="hotdog">
  <p>...</p>
  <p>...</p>
  <p class="mustard">...</p>
</div>
```

#### CSS
```css
.hotdog p {
  backgound: brown;
}
.hotdog p.mustard {
  background: yellow;
}
```

The first selector *.hotdog p* is a class and a type selector. The *p* type selector is the key selector, but it is prequalified by a *.hotdog* class selector so the whole style will target only paragraphs that are within a element with the hotdog class attribute.

The second selector has a key selector of *.mustard* and while *p* and *.hotdog* are prequalifiers.

### Spaces Within Selectors
In the second selector, there is no space between p.mustard, which means that the selector with only style p elements with the class of mustard.

***Best Practice is to not prequalify a class***

### Specifitcity with Combined Selectors
Looking back at *.hotdog p*, there is a class selector and a type selector giving it a specificity of 0-1-1.

The second selector *.hotdog p.mustard*, has two class selectors and a type selector giving it a specificy of 0-2-1.

**This means the second selector with always take precedence in a style conflict**

## Layering Styles with Multiple Classes
We need to keep our specificity weight low so we will layer our styles with multiple classes.

HTML Elements can support multiple classes as long as they are space separated.

#### HTML
```html
<a class="btn btn-danger">...</a>
<a class="btn btn-success">...</a>
```

#### CSS
```css
.btn {
  font-size: 16px;
}
.btn-danger {
  background: red;
}
.btn-success {
  background: green;
}
```

Since both elements share *.btn* they will both have 16px font but the seconde class they have is different allowing us to have different colors on the buttons and our specificity is kept low so they won't overrule each other.

## Common CSS Property Values
There are a handful of common CSS properties, but right now we are just focusing on color and length.

### Colors
There are four primary ways to represent color in CSS

#### Keyword Colors
Keyword color is when you use the colors name to represent it.

A list can be found at [CSS Color Module](https://www.w3.org/TR/css-color-3/#svg-color)

Example of using keyword coloring:

##### CSS
```css
.task {
  background: maroon;
}
.count {
  background: yellow;
}
```

#### Hexadecimal Colors
Hexidemimal Colors are represented by 3 or 6 characters preceded by a *#*

In the 6 character notation, the first 2 digits are for red, next 2 are for green, and the last 2 are for blue.

If each pair is matching digits, then you can just use 3 character notation by using each pair's character once.

Example of hexidecimal:

##### CSS
```css
.task {
  background: #800000;
}
.count {
  background: #ff0;
}
```

A good tool for hexidecimal color finding is [Adobe Color CC](https://color.adobe.com/)

#### RGB & RGBa Colors
RGB colors are represented by using *rgb()* with 3 comma separated integers ranging from 0 to 255 representing amounts of red, green, and blue.

Example of RGB Colors:

##### CSS
```css
.task {
  background: rgb(128, 0, 0);
}
.count {
  background: rgb(255, 255, 0);
}
```

RGBa colors include an alpha value that can be any decimal value from 0 to 1 which represents the trasparency of the color.

Example of RGBa Colors:

##### CSS
```css
.tack {
  background: rgba(128, 0, 0, .25);
}
.count {
  background: rgba(128, 0, 0, 1);
}
```

#### HSL & HSLa Colors
HSL colors are represented by using *hsl()* with 3 values
  * The first value represents the hue using an integer ranging 0 to 360.
  * The second and third values represent the saturation and lightness, using a percentage from 0% to 100%.
  
Example of using HSL Colors:
  
##### CSS
```css
.task {
  background: hsl(0, 100%, 25%)
}
.count {
  background: hsl(60, 100%, 50%)
}
```

HSLa colors include a alpha value like RGBa.

Example of using HSLa Colors:

##### CSS
```css
.task {
  background: hsla(0, 100%, 25%, .25)
}
.count {
  background: hsla(60, 100%, 50%, 1);
}
```

### Lengths
Length values come in two different forms: *absolute* and *relative*
*This is a list of the more common and straight forward, there will be more later*

#### Absolute Lengths
Absolute lengths are fixed to a physical measurement.

##### Pixels
A pixel is 1/96th of an inch, but can differ by display.

Example of using pixel length:

###### CSS
```css
p {
  font-size: 14px;
}
```

#### Relative Lengths
Relative measurements rely on the measurement of something else.

##### Percentages
Percentage is represented by the % unit notation and adjusts the length based on the property given.

If width is given the length of 50% then the width will be set to 50% of the parent element.

Example of using percentage length:

###### CSS
```css
.col {
  width: 50%;
}
```

##### Em
The em unit is represented by *em* unit notation and is equivalent to a element's font size.

Example of using em length:

###### CSS
```css
.banner {
  font-size: 14px;
  width: 5em;
}
```

If font size isnot explicitly stated, em will equal the font size of the closet parent element.
