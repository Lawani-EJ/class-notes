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
    <a href="about.html">Learn more about the Astronomy Club </a>
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


# Audio and Videos 
The <`video>` and `<audio>` elements can be used to embed media players directly with the src attribute or can be used as the container element for a series of `<source>` elements, each providing a `src` file suggestion.
The opening `<video>` and `<audio>` tags can contain several other attributes including `controls`, `autoplay`, `loop`, `mute`, `preload`, and the global attributes. The `<video>` element also supports the `height`,` width`, and `poster` attributes.

```html
<video src="videos/machines.webm" poster="images/machine.jpg" controls>
  <p>Watch <a href="https://youtube.com/link">video on Youtube</a></p>
</video>
```

# Template, slot, and shadow
The benefit of web components is their re-usability: you can create a UI widget once, and reuse it multiple times. While you do need JavaScript to create web components, you don't need a JavaScript library. HTML and the associated APIs provide everything you need.

In this section, we'll create the <star-rating> element, a web component that allows users to rate an experience on a scale of one to five stars. When naming a custom element, it is recommended to use all lowercase letters. Also, include a dash, as this helps distinguish between regular and custom elements.


### Template Element
The `<template>` element is used to declare fragments of HTML to be cloned and inserted into the DOM with JavaScript. The contents of the element are not rendered by default. Rather, they are instantiated using JavaScript.

```
<template id="star-rating-template">
  <form>
    <fieldset>
      <legend>Rate your experience:</legend>
      <rating>
        <input type="radio" name="rating" value="1" aria-label="1 star" required />
        <input type="radio" name="rating" value="2" aria-label="2 stars" />
        <input type="radio" name="rating" value="3" aria-label="3 stars" />
        <input type="radio" name="rating" value="4" aria-label="4 stars" />
        <input type="radio" name="rating" value="5" aria-label="5 stars" />
      </rating>
    </fieldset>
    <button type="reset">Reset</button>
    <button type="submit">Submit</button>
  </form>
</template>
```

As the contents of a <template> element are not written to the screen, the <form> and its contents aren't rendered. Yes, this Codepen is blank, but if you inspect the HTML tab, you'll see the <template> markup.
In this example, the `<form>` is not a child of a `<template>` in the DOM. Rather, contents of `<template>` elements are children of a DocumentFragment returned by the HTMLTemplateElement.content property. To be made visible, JavaScript must be used to grab the contents and append those contents to the DOM.


```

let starRating = document.getElementById("star-rating-template").content;
document.body.appendChild(starRating);

```

This brief JavaScript did not create a custom element. Rather, this example has appended the contents of the <template> into the <body>. The content has become part of the visible, styleable DOM.

### Slot Element
We include a slot to include a customized per occurrence legend. HTML provides a ```<slot>``` element as a placeholder inside a ```<template>``` that, if provided a name, creates a "named slot".

```Html
<template id="star-rating-template">
  <form>
    <fieldset>
      <slot name="star-rating-legend">
        <legend>Rate your experience:</legend>
      </slot>
```

The primary purpose of ```<slot>``` is to allow a parent component to "project" or insert its own content into specific areas within a child web component's template.

By assigning a name attribute to a ```<slot>```, you create a "named slot." This allows the parent component to target specific slots by using the slot attribute on its child elements, matching the name of the desired slot.

# HTML API'S
In the introduction to this series it says "HTML elements are the nodes that make up the Document Object Model." We've discussed the type of element nodes. In this section we discuss element APIs that enable querying those nodes.

### The DOM and AOM
## DOM (Document Object Model)
What it is : The DOM is a programming interface for HTML and XML documents that represents the document structure as a tree of objects.

How it works: Each part of the document, such as elements, attributes, and texts is a "node" in the tree.

Primary use: Allows scripts to dynamically change the content, structure, and style of a web page after it is loaded.

Example: A JavaScript script can use the DOM to find a button and then change the text of a paragraph when a button is clicked.

## AOM (Accesibility Object Model)

What it is: The AOM is a proposed web API that provides programmatic access to the accessibility tree, a semantic representation of the DOM used by assistive technologies.

How it works: The browser automatically builds this tree from the DOM, and the AOM is intended to let developers interact with it.

Primary use: To ensure that web content is accessible to all users, particullarly those who rely on assistive devices like screen readers.

Example: A developer can use the AOM to expose the semantic roles and relationships of custom "Web Components" to the accesibility tree.


# HTML Element APIs
The key element in API's is that JavaScript Interfaces are able to be manipulated and interacted by developers within a webpage.

## Some aspects in HTML Element API's :
- DOM Manipulation.
- Event Handling.
- Styling and Attributes.
- HTML5 API's.

  # DOM Manipulation
  The core of HTML Elments API's revolves around the Document Object Model (DOM). The DOM represents the structure of the HTML document as a tree of objects, and these API's provide methods to access, modify, add, and remove elements and their content.

```Javascript
  // Accessing an element by ID and changing its content
  const myElement =  document.getElementById('myDiv');
  myElement.innerHTML = 'New Content goes here!!';
```

# Why API's are important
1. APIs help developers integrate exciting features and build automation without reinventing the wheel
2. APIs allow enterprises to open up their product for faster innovation
3. APIs can be products themselves

## The types of API
- Hardware API's
- Software Library API's
- Web API's

1. Hardware API's : Interface for software to talk to hardware.
2. Software Library API's : Interface for directly consuming code from another code base.
3. Web API's: Interface for communicating across code bases over a network.

Multiple API types may be used to achieve a task. For example, uploading a photo to instagram makes use of various API's
- Hardware API for the app to talk to your camera.
- Software Library API for the image to be processed with filters.
- Web API for sending your image to instagram's servers so your friends can like it.

## Access
API's also vary in the scope of who can access them

- Public API's (also known as open API's) : Consumed by anyone who discovers the API.
- Private API's: Consumed only within an organization and not made public.
- Partner API's : Consumed by one or more organizations that have an established relationship.

# An API Plattform
Postman is an API plattform that is used for for building and testing API's. With Postman i can simplify the steps and process of each API lifecycle and streamline my colloborations so that i can create better API's faster and consume them with ease.

# Working with API's then and now: Curl vs Postman
Before Postman it was common practice to poke at API's with a command line tool for making HTTP requests called cURL. This tool is still used today but has it's limitations when it comes to colloborating and sharing.

This is an example of what an API call in the terminal using the `curl` command looks like. Here we are fetching data about GitHub user postmanlabs.

curl https://api.github.com/users/postmanlabs

<img width="1128" height="1080" alt="image" src="https://github.com/user-attachments/assets/f8433b66-da5e-4a9e-8fb8-4202ec753b6d" />

It works great, but once you make the call, the API response data is lost in the river of the terminal. You also don't have visibility of the metadata of the response without adding more details to the command.

## API calls with Postman
 Postman shows the response with clean indents and colors and allows you to save, organize and share your requests. You can also see all the components of the request and response broken down into tabs and other helpful details like the response time and status code. 

 <img width="1575" height="1080" alt="image" src="https://github.com/user-attachments/assets/21557246-6dcc-44c9-8f4e-ab41309b6a33" />

# Request Methods
When we make an HTTP call to a server, we specify a request method that indicates the type of operation we are about to perform. These are also called HTTP Verbs.

Some common HTTP request methods correspond to the CRUD operations

| Method Name | Operation               |
|-------------|--------------------------|
| GET         | Retrieve data (Read)     |
| POST        | Send data (Create)       |
| PUT / PATCH | Update data (Update)     |
| DELETE      | Delete data (Delete)     |

> **Note:**  
> - **PUT** usually replaces an entire resource.  
> - **PATCH** is typically used for partial updates.

# Response Status codes
Status codes have conventions. For example, any status code with a  "2xx" (a "200-level response") represents a succesful call.

| Code Range | Meaning        | Examples                                   |
|------------|----------------|---------------------------------------------|
| **2xx**    | Success        | 200 – OK  
|            |                | 201 – Created  
|            |                | 204 – No Content (silent OK)               |
| **3xx**    | Redirection    | 301 – Moved (path changed)                 |
| **4xx**    | Client Error   | 400 – Bad Request  
|            |                | 401 – Unauthorized  
|            |                | 403 – Not Permitted  
|            |                | 404 – Not Found                            |
| **5xx**    | Server Error   | 500 – Internal Server Error  
|            |                | 502 – Bad Gateway  
|            |                | 504 – Gateway Timeout                      |

# Query Parameters
Some APIs allow you to refine your request further with key-value pairs called query parameters.  
Query parameters are added to the end of the path. They start with a question mark ``?`` followed by the key-value pairs in the format ```<key>=<value>```.

```GET https://some-api.com/photos?orientation=landscape```

For example this request might fetch all photos that have a landscape orientation, if there are multiple query parameters, each is seperated by an ampersand ```&```.

# When to use Query parameters
The right answer to use is always. Sometimes query parameters are optional and allow you to add filters or extra data responses. Sometimes they are required in order for the server to process your request. API are implemeted differently to fufil different needs.
