# CSS Layout
### Website Layout
A website is often divided into headers, menus, content and a footer:

![Image](https://media.geeksforgeeks.org/wp-content/uploads/website_layout-300x268.png)

### Header Section
The header section is generally placed either at the top of the Website or just below a top navigation menu. It often comprises of the name of the Website or the logo of the Website.

### Navigation Menu
A Navigation Bar/Menu is basically a list of links that allows visitor to navigate through the website comfortably with easy access.

### Content Section
The content section is the main body of the website. The user can divide content section in n-column layout.

### Footer Section 
A footer section is placed at the bottom of the webpage and it generally consists of information like contact info, copyrights, About us etc.


# CSS layouts:
## Prerequisites

## Guides:

CSS page layout techniques allow us to take elements contained in a web page and control where they are positioned relative to their default position in normal layout flow, the other elements around them, their parent container, or the main viewport/window.  The page layout techniques we'll be covering in more detail in this module are:


##  Normal flow
Normal flow is how the browser lays out HTML pages by default when you do nothing to control page layout. Let's look at a quick HTML example:

```html
<p>I love music</p>

<ul>
  <li>Listen to my favorite Song </li>
  <li>Exercise</li>
  <li>Cheer up friend</li>
</ul>

<p>The end!</p>

```
by default the browser will appeare it as unorderd list, as you notice here that is how the HTML is displayed in the exact order in which it appears in the source code, with elements stacked up on top of one another — `the first paragraph`, followed by `the unordered list`, followed by `the second paragraph.`

The elements that appear one below the other are described as *block elements*, in contrast to *inline elements*, which appear one beside the other, like the individual words in a paragraph.

**The methods that can change how elements are laid out in CSS are as follows:**

- **The display property** — Standard values such as block, inline or inline-block can change how elements behave in normal flow, for example making a block-level element behave like an inline element (see Types of CSS boxes for more information). We also have entire layout methods that are switched on via specific display values, for example CSS Grid and Flexbox, which alter how elements inside the element they are set on are laid out.
- **Floats** — Applying a float value such as left can cause block level elements to wrap alongside one side of an element, like the way images sometimes have text floating around them in magazine layouts.
- **The position property** — Allows you to precisely control the placement of boxes inside other boxes. static positioning is the default in normal flow, but you can cause elements to be laid out differently using other values, for example always fixed to the top of the browser viewport.
- **Table layout** — features designed for styling the parts of an HTML table can be used on non-table elements using `display: table` and associated properties.
- **Multi-column layout** — The Multi-column layout properties can cause the content of a block to layout in columns, as you might see in a newspaper.

## Flexbox
**Flexbox (Flexible Box Layout Module)**, designed to make it easy for us to lay things out in one dimension — either as a row or as a column. To use flexbox, you apply `display: flex` to the parent element of the elements you want to lay out; all its direct children then become flex items.



## Grid Layout
While flexbox is designed for one-dimensional layout, Grid Layout is designed for two dimensions — lining things up in rows and columns.

Once again, you can switch on Grid Layout with a specific value of display — `display: grid`. 

## Floats
Floating an element changes the behavior of that element and the block level elements that follow it in normal flow.
The float property has four possible values:

- `left` — Floats the element to the left.
- `right` — Floats the element to the right.
- `none` — Specifies no floating at all. This is the default value.
- `inherit` — Specifies that the value of the float property should be inherited from the element's parent element.

## Positioning techniques
There are five types of positioning you should know about:

- **Static positioning** is the default that every element gets — it just means "put the element into its normal position in the document layout flow — nothing special to see here".
- **Relative positioning** allows you to modify an element's position on the page, moving it relative to its position in normal flow — including making it overlap other elements on the page.
- **Absolute positioning** moves an element completely out of the page's normal layout flow, like it is sitting on its own separate layer. From there, you can fix it in a position relative to the edges of the page's <html> element (or its nearest positioned ancestor element). This is useful for creating complex layout effects such as tabbed boxes where different content panels sit on top of one another and are shown and hidden as desired, or information panels that sit off screen by default, but can be made to slide on screen using a control button.
- **Fixed positioning** is very similar to absolute positioning, except that it fixes an element relative to the browser viewport, not another element. This is useful for creating effects such as a persistent navigation menu that always stays in the same place on the screen as the rest of the content scrolls.
- **Sticky positioning** is a newer positioning method which makes an element act like position: static until it hits a defined offset from the viewport, at which point it acts like position: fixed.


## Table layout
The way that a table looks on a webpage when you use table markup is due to a set of CSS properties that define table layout. These properties can be used to lay out elements that are not tables, a use which is sometimes described as "using CSS tables".

Most of the CSS is fairly ordinary, except for the uses of the display property. The `<form>`, `<div>`s, and `<label>`s and `<input>`s have been told to display like a table, table rows, and table cells respectively — basically, they'll act like HTML table markup, causing the labels and inputs to line up nicely by default. All we then have to do is add a bit of sizing, margin, etc. to make everything look a bit nicer and we're done.

You'll notice that the caption paragraph has been given `display: table-caption`; — which makes it act like a table `<caption>` — and caption-side: bottom; to tell the caption to sit on the bottom of the table for styling purposes, even though the markup is before the `<input>`<input> elements in the source. _This allows for a nice bit of flexibility.