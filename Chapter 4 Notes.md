# *Notes* Chapter 4: Opening the Box Model

## How Are Elements Displayed?

### Display

Every element has a default *display* property that determines how they are displayed and because it is a property it can be overwritten.

There are a lot of possible values for *display* but the most common are *block*, *inline*, *inline-block*, and *none*.

Examples of changing the display property:

#### CSS
```css
p {
	display: inline;
}
p {
	display: block;
}
p {
	display: inline-block;
}
p {
	display: none;
}
```

* *Inline* makes an element act as an inline element.
* *Block* makes an element act as a block element.
* *Inline-block* will allow the element to receive all box model properties but still appeare in line and not begin on a new line.
* *None* will hide the element and all children of that element.

