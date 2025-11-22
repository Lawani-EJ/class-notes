# class-notes <LEARNING HTML> 😩😭😩
These are some notes i take during classes 

- [x] Internet:
The internet is a group of interconnected computers using TCP/IP protocols, connecting billions of devivces worldwide.

- [x] How does the information move on the internet?
Wires, cables and WiFi, information on the internet moves from one computer to another in the form of bits over various mediums including Etherum cables, fiber optic cables and wireless signals (i.e. Radio waves)

- [x] What is HTTP: Hyper Text Transfer Protocol enables browser-server communication through requests and responses. The Hypertext Transfer Protocol is used to load pages on the Internet using hyperlinks.

- [x] Overview of HTML :
- HyperText Markup Language, or HTML, is the standard markup language for describing the structure of documents displayed on the web.

## Very Important explanantion of HTML: 
HyperText Markup Language 
1. Hyper Text: This a network of interconnected documents.Refers to text that contains links to other text or resources.
2. Markup: A markup language uses tags to define the structure and formatting of a document.
3. Language: "language" refers to a system of vocabulary and syntax (rules) used to create documents that can be understood by a web browser.

In essence, HTML is the language used to create the structure and content of web pages. It uses tags to define elements like headings, paragraphs, lists, images, and links.

- [x] HTML Elemements
- HTML consists of a series of elements, which you use to enclose, or wrap, different parts of the content to make it appear or act in a certain way. HTML elements are delineated by tags, written using angle brackets (< and >).

<img width="4152" height="1644" alt="image" src="https://github.com/user-attachments/assets/5e4a3bda-ec7c-42b3-9d47-b903b811cd88" />

Some omitted closing tags cause bigger issues: not closing some tags, such as <script>, <style>, <template>, <textarea>, and <title>, breaks subsequent content as shown in the following example.

```html
<p>If you add <strong>Strong</oops> text and <em>emphasised</doh> text but forget to close your tags, that doesn't cause the worst problems.</ohno>
<p>All that happens is your text continue to be bold and emphasized.</ohno>

<p>But not closing a `style` or `script` is a more serious issue. 
  <p>The script only shows because we changed the display.
  <style>
    p {
      color:red;
    }
    style {
      display: unset;
     }
  <p>text coming after 
  <table>
    <tr>
      <th>Optional closing
    <tr>
      <td>table cell
```

## Important notes:
There are two types of elements: replaced and non-replaced.

### Non-replaced elements:
The paragraph, header, and lists marked up in the earlier section are all non-replaced. Non-replaced elements have opening and (sometimes optional) closing tags that surround them and may include text and other tags as sub-elements.

### Replacable elements:
In web development, replaced elements are HTML elements whose content are replaced by external resources or content defined outside of the document structure, and are not considered in the CSS rendering model. 
The following can be replaced elements:
```html
<img>
<video>
<iframe>
<embed>
<fencedframe>
```

## HTML Document Structure:
HTML documents include a document type declaration and the <html> root element. Nested in the <html> element are the document head and document body. 

### Add to every HTML Document:
1. The first thing in any HTML document is the preamble. ```<!DOCTYPE html>``` tells the browser to use standards mode. If omitted, browsers will use a         different rendering mode known as quirks mode.
2. The ```<html>``` element is the root element for an HTML document. It is the parent of the ```<head>``` and ```<body>```, containing everything in the HTML document other than the doctype.
3. The lang language attribute added to the ```<html>``` tag defines the main language of the document.  For example, French is very different in Canada (fr-CA) versus Burkina Faso (fr-BF). This language declaration enables screen readers, search engines, and translation services to know the document language.

```HTML
<!DOCTYPE html>
<html lang="en-US">
  <head>
  </head>
  <body>
  </body>
</html>
```

The head contains all the metadata for a site or application. While the body contains all the visible content.
## The required components inside the head:
1. The character encoding. ```<meta charset="utf-8" />``` to ensure the browser can render the characters in that title and all the characters in the rest of the document.

Reference: `https://gorails.com/episodes/html-learning-path-html-document-structure?ref=dailydev`

2. The Document title:
Your home page and all additional pages should each have a unique title. ```<title>Machine Learning Workshop</title>```

3. The viewport metadata:
 it enables controlling a viewport's size and scale, and prevents the site's content from being sized down to fit a 960px site onto a 320px screen, it is definitely recommended. ```<meta name="viewport" content="width=device-width" />``` The preceding code means "make the site responsive, starting by making the width of the content the width of the screen".

So far, the outline for our HTML file is:
```HTNL
<!DOCTYPE html>
<html>
<head>
  <title>My First Web Page</title>
</head>
<body>
  <h1>Hello, World!</h1>
  <p>This is my first web page.</p>
</body>
</html>
```

# Headings and sections
## Site `<header>`

    <!-- start header -->
    <div id="pageHeader">
      <div id="title">Machine Learning Workshop</div>
      <!-- navigation -->
      <div id="navigation">
        <a href="#reg">Register</a>
        <a href="#about">About</a>
        <a href="#teachers">Instructors</a>
        <a href="#feedback">Testimonials</a>
      </div>
      <!-- end navigation bar -->
    </div>
    <!-- end of header -->

You can include `role` attributes to provide semantics to create a good accessibility object model (AOM) for screen readers:  

    <!-- start header -->
    <div role="banner">
      <div role="heading" aria-level="1">Machine Learning Workshop</div>
      <div role="navigation">
        <a href="#reg">Register</a>
        <a href="#about">About</a>
        <a href="#teachers">Instructors</a>
        <a href="#feedback">Testimonials</a>
      </div>
      <!-- end navigation bar -->
    <div>
    <!-- end of header -->


CSS can make (almost) any markup look right. But using the non-semantic `<div>` for everything actually creates extra work. To target multiple `<div>`s with CSS, you end up using ids or classes to identify the content. The code also includes a comment for each closing `</div>` to indicate which opening tag each `</div>` closed.

While the `id` and `class` attributes provide hooks for styling and JavaScript, they add no semantic value for the screen reader and (for the most part) the search engines.


# CSS
The ```<head>``` is where you include styles for your HTML. There are three ways to include CSS: ```<link>```, ```<style>```, and the ```style``` attribute. 
1.The `<link>` tag is the most preferable method of icluding sylesheets. The syntax is `<link rel="stylesheet" href="styles.css">`, where styles.css is the URL of your stylesheet.
The ``rel`` attribute defines the relationship: in this case ```stylesheet```. If you omit this, your CSS will not be linked.

2. The ```style``` is used when we want our style sheet to be within a cascade (poured on) layer but want to access and edit the file we include the the CSS with the ```@import``` inside a style

 ```HTML
<style>
  @import "styles.css" layer(firstLayer);
</style>
```

# Links 
Hyperlinks, often referred to simply as 'links', connect various parts of a website, different files, or even other websites, providing a seamless navigation experience. In HTML, we create these essential navigational devices using the <a> tag coupled with an href attribute that specifies the destination of the link.

``` HTML
<!DOCTYPE html>
<html>
<head>
    <title>Space Exploration</title>
</head>
<body>
    <h1>Welcome to the Astronomy Club</h1>
    <!-- Create a link to a page about the Solar System. Don't forget to make it open in a new tab! Here is a sample URL you can use: https://en.wikipedia.org/wiki/Solar_System -->
    <a href="https://en.wikipedia.org/wiki/Solar_System" target="_blank">Link to a page about the solar system..</a>

    <!-- Create a link to the about.html page that is already predefined -->
    <a href="about.html">Learn more about the Astronomy Club 🚀</a>
</body>
</html>
```

# Images
The ```<img>``` tag is an HTML element used to embed an image into a web page.

```
<img src="https://images.unsplash.com/photo-1519681393784-a939888cd496?ixlib=rb-1.2.1&auto=format&fit=crop&w=1050&q=80">
```

# All about attributes:
Attributes define the behavior, linkages, and functionality of elements. 

```HTML
<!-- the type attribute is case insensitive: these are equivalent -->
<input type="text">
<input type="TeXt">

<!-- the id attribute is case sensitive: they are not equivalent -->
<div id="myId">
<div id="MyID">
```

## Other Attributes include:
1. Boolean Attribute: If a boolean attribute is always present then it is always true.
2. Global Attribute: Are attributes that can be set on any HTML element, including elements in the head.
3. Enumerated Attribute: They have a limited set of predifined valid values. Eg, If you include ```<style contenteditable="false">```, the element is not editable. If the value is invalid, such as ```<style contenteditable="😀">```, or, surprisingly, ```<style contenteditable="contenteditable">```, the value is invalid and defaults to inherit.

## Lists
Lists are more common than you might think. If you've ever taken a programming class, the first project may have been to create a shopping list or a to-do list. Those are lists. Multiple-choice tests are generally numbered lists of questions: the multiple possible answers for each question are nested lists.

1. Unordered Lists
2. Ordered Lists
3. Description Lists

# Tables
The `<table>` tag wraps the table content, including all the table elements.
The table's children are, in order:
1. `<caption>` element
2. `<colgroup>` elements
3. `<thead>` elements
4. `<tbody>` elements
5. `<tfoot>` elements

# Important Class

# Forms
With forms, you can enable users to interact with your website or application, validate the information entered, and submit the data to a server.

## Submitting forms 
```
<input type="submit" value="Submit Form">
<button type="submit">Submit Form</button>
```

Forms are submitted when the user activates a submit button nested within the form. When using <input> for buttons, the 'value' is the button's label, and is displayed in the button. When using <button>, the label is the text between the opening and closing <button> tags.


# Images and Videos 