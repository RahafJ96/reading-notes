# HTML and Wireframes

## What is Wireframes?
Wireframing is a practice which allows them to define and plan the information steps of their design for a website, application, or product. This process focuses on how the designer or client wants the user to process information on a site, based on the user research already performed by the UX design team.
As shown bellow:
![Image](https://d33wubrfki0l68.cloudfront.net/dbb80f2f6a5dafa25f702ad00bc429057fb59cec/52716/en/blog/uploads/versions/samuel-student-wireframe---x----972-715x---.png)

### How to create a simple and understandable Wireframe:
**1. Clarity**

Your wireframe needs to answer the questions of what that site page is, what the user can do there, and if it satisfies their needs.

**2. Confidence**

Ease of navigation through your site and clear calls-to-action increase user confidence in your brand

**3. Simplify as much as possilbe**

Your wireframe should be a visual guide to the framework of your site and how it will be navigated.By presenting your information in this way, you are aligning both the business goals of your site with the needs of the customer.


# What is HTML?

HTML is *a markup language that defines the structure of your content. * 

HTML elements are the building blocks of HTML pages.

- **<!DOCTYPE html>** declaration defines this document to be HTML5
- **<html>** element is the root element of an HTML page
- **The lang attribute**  defines the language of the document
- **The <meta> element** contains meta information about the document
- **The <title> element** specifies a title for the document
- **<body> element** contains the visible page content
- **<h1>** element defines a large heading
- **<p>** element defines a paragraph

### HTML Document Structure
![Image](https://codescracker.com/html/images/html-document-structure-example.jpg)

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

## Defining functions:
JavaScript functions are defined with the function keyword. It can be used as a function declaration or a function expression. 
The construction of the function:
- The name of the function.
- A list of commands to the function, surrounded in parentheses and separated by commas.
- The JavaScript statements that define the function, enclosed in curly brackets, {...}.

_function nameOfTheFuntion(p1, p2) {
  return p1 * p2;   // The function returns the product of p1 and p2
}_

