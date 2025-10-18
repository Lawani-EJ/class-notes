# class-notes <LEARNING HTML> 😩😭😩
These are some notes i take during classes 

- [x] Internet:
The internet is a group of interconnected computers using TCP/IP protocols, connecting billions of devivces worldwide.

- [x] How does the information move on the internet?
Wires, cables and WiFi, information on the internet moves from one computer to another in the form of bits over various mediums including Etherum cables, fiber optic cables and wireless signals (i.e. Radio waves)

- [x] What is HTTP: Hyper Text Transfer Protocol enables browser-server communication through requests and responses. The Hypertext Transfer Protocol is used to load pages on the Internet using hyperlinks.

- [x] Overview of HTML :
- HyperText Markup Language, or HTML, is the standard markup language for describing the structure of documents displayed on the web.

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
