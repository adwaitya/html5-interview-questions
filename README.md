
# HTML5 Interview Questions and Answers

*Click <img src="assets/star.png" width="18" height="18" align="absmiddle" title="Star" /> if you like the project.


<br/>

|Sl.No|  Questions                        |
|----|------------------------------------|
| 01.|[What is the WHATWG?](#q-what-is-the-WHATWG)|
| 02.|[What is an iframe and how it works?](#q-what-is-an-iframe-and-how-it-works?)|
| 03.|[How do you set language in HTML?](#q-how-do-you-set-language-in-HTML?)|
| 04.|[What is the DOM? How does the DOM work?](#q-what-is-the-dom-how-does-the-dom-work)|
| 05.|[How does the browser rendering engine work?](#q-how-does-the-browser-rendering-engine-work)|
| 06.|[What does a `<DOCTYPE html>` do?](#q-what-does-a-doctype-html-do)|
| 07.|[What happens when DOCTYPE is not given?](#q-what-happens-when-doctype-is-not-given)|


<br/>



## Q. ***What is the WHATWG??***
-   The Web Hypertext Application Technology Working Group (WHATWG) is a community of people interested in evolving the web through standards and tests.
-   The WHATWG was founded by individuals of Apple, the Mozilla Foundation, and Opera Software in 2004, after a W3C workshop. Apple, Mozilla and Opera were becoming increasingly concerned about the W3C’s direction with XHTML, lack of interest in HTML, and apparent disregard for the needs of real-world web developers. So, in response, these organisations set out with a mission to address these concerns and the Web Hypertext Application Technology Working Group was born

## Q. ***What is an iframe and how it works?***
* An iframe is an HTML document which can be embedded inside another HTML page
**Example:*
```html
<iframe src="https://github.com" height="300px" width="300px"></iframe>
```

## Q. ***How do you set language in HTML?***
There are multiple ways to set language in HTML
*   By setting content-language in headers for language of the page
*   By setting accept-language in headers for list of language that a page accept
*   Setting lang attribute in html tag

**Example:*
```HTML
<!DOCTYPE html>
<html lang="en">
<head>
  <title>Document Title</title>
</head>
<body>

</body>
</html>
```

## Q. ***What is the DOM? How does the DOM work?*** 

The DOM (Document Object Model) is a cross-platform API that treats HTML documents as a tree structure consisting of nodes. These nodes (such as elements and text nodes) are objects that can be programmatically manipulated and any visible changes made to them are reflected live in the document. In a browser, this API is available to JavaScript where DOM nodes can be manipulated to change their styles, contents, placement in the document, or interacted with through event listeners.

* When a browser loads web page, then browser create the document object model for the page.

* The DOM was designed to be independent of any particular programming language, making the structural representation of the document available from a single, consistent API.

* document.getElementById() and document.querySelector() are common functions for selecting DOM nodes.

* Setting the innerHTML property to a new value runs the string through the HTML parser, offering an easy way to append dynamic HTML content to a node.


## Q. ***How does the browser rendering engine work?***

In order to render content the browser has to go through a series of steps:

* Document Object Model(DOM)
* CSS object model(CSSOM)
* Render Tree
* Layout
* Paint

<img src="assets/layers.png" alt="Browser Rendering Engine" />

<div align="right">
    <b><a href="#">↥ back to top</a></b>
</div>

## Q. ***What does a `<DOCTYPE html>` do?***

A DOCTYPE is always associated to a `DTD` ( **Document Type Definition** ). A DTD defines how documents of a certain type should be structured (i.e. a `button` can contain a `span` but not a `div`), whereas a DOCTYPE declares what DTD a document supposedly respects (i.e. this document respects the HTML DTD). For webpages, the DOCTYPE declaration is required. It is used to tell user agents what version of the HTML specifications your document respects. 

Once a user agent has recognized a correct DOCTYPE, it will trigger the `no-quirks mode` matching this DOCTYPE forreading the document. If a user agent doesn't recognize a correct DOCTYPE, it will trigger the `quirks mode`.

## Q. ***What happens when DOCTYPE is not given?***

The web page is rendered in quirks mode. The web browsers engines use quirks mode to support older browsers which does not follow the **W3C specifications**. In quirks mode CSS class and id names are case insensitive. In standards mode they are case sensitive.
<div align="right">
    <b><a href="#">↥ back to top</a></b>
</div>
