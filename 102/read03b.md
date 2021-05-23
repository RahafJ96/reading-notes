# Design web pages with CSS

## What is CSS?
- **CSS** stands for Cascading Style Sheets
- **CSS** describes how HTML elements are to be displayed on screen, paper, or in other media
- **CSS** saves a lot of work. It can control the layout of multiple web pages all at once
- External stylesheets are stored in CSS files.

## Why  CSS?
CSS is *used to define styles for your web pages, including the design layout and variations in display for different devices and screen sizes.* 

* HTML was NEVER intended to contain tags for formatting a web page!
* HTML was created to describe the content of a web page, like:
<h1>This is a heading</h1>
<p>This is a paragraph.</p>

* When tags like <font>, and color attributes were added to the HTML, it started a nightmare for web developers. Development of large websites, where fonts and color information were added to every single page, became a long and expensive process.

- **To solve this problem, the World Wide Web Consortium (W3C) created CSS.** **_CSS removed the style formatting from the HTML page!_**

### Cascading Order
All the styles in a page will "cascade" into a new "virtual" style sheet by the following rules, where number one has the highest priority:

1. Inline style (inside an HTML element)
2. External and internal style sheets (in the head section)
3. Browser default

So, an inline style has the highest priority, and will override external and internal styles and browser defaults.


### Some notes should be considered:
- We use the Link tag to Link Css file with the HTML file, as:
_<link rel="stylesheet" href="mystyle.css">_

- example of CSS syntax:
*body{
background-color: whitesmoke;
margin: 0%
}*

*header{
  color: whitesmoke;
height: 80% ;
}*

*header{
  float: right;
  width: 30%;
  margin-top: -24px;
}*

*body{
  text-align: center;
  font-size: 40px;
}*

### **Colors in CSS**
**CSS color Property:**

body {
  color: red;
}

h1 {
  color: #00ff00;
}

p.ex {
  color: rgb(0,0,255);
}

_We used in our project [colorhunt](https://colorhunt.co/)_

