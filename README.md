
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
| 08.|[What are the building blocks of HTML5?](#q-what-are-the-building-blocks-of-html5)|
| 09.|[Describe the difference between a `cookie`, `sessionStorage` and `localStorage`?](#q-describe-the-difference-between-a-cookie-sessionstorage-and-localstorage)

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

**Example:**
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

***The W3C Document Object Model (DOM) is a platform and language-neutral interface that allows programs and scripts to dynamically access and update the content, structure, and style of a document.***

Confused? Let me make that simple. Imagine that, every web page is a document and every element( be it text or image or table) inside that webpage is stored in that document as an object in a tree format, which can be manipulated later with a scripting language such as JavaScript. \
<img src="assets/dom1.png" alt="Dom" /> \
Now, when a web page is loaded, the browser creates such a document every time which is called, Document Object Model (DOM) of the page.\
The DOM represents the document as nodes and objects so that programs can change the document structure, style, and content. In that hat way, programming languages connect to the webpage.
<div align="right">
    <b><a href="#">↥ back to top</a></b>
</div>


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

Doctype is the abbreviation for the “Document type”. The very first line in every web document should contain a <!DOCTYPE html> declaration. \
The purpose of DOCTYPE is to tell the browser what type of HTML you are writing. It is not valid to omit the DOCTYPE. There is no “Standard” format. The browser will just try to parse HTML as best it can. But not all elements will be displayed correctly. DOCTYPE is a required part of all HTML documents.\
To render a HTML4.01 document, use this code at the very top of your document:
```HTML
<!DOCTYPE HTML PUBLIC “-//W3C//DTD HTML 4.01//EN” “http://www.w3.org/TR/html4/strict.dtd">
```
To render a HTML5 document, include this code instead:\
<!doctype html>\
The Doctype declaration informs the web browser about the type and version of HTML used in building the web document (e.g. HTML5, HTML4.0, XHTML1.0)\
<div align="right">
    <b><a href="#">↥ back to top</a></b>
</div>

## Q. ***What happens when DOCTYPE is not given?***

The web page is rendered in quirks mode. The web browsers engines use quirks mode to support older browsers which does not follow the **W3C specifications**. In quirks mode CSS class and id names are case insensitive. In standards mode they are case sensitive.
<div align="right">
    <b><a href="#">↥ back to top</a></b>
</div>

## Q. ***What are the building blocks of HTML5?***

* **Semantics**: allowing you to describe more precisely what your content is.
* **Connectivity**: allowing you to communicate with the server in new and innovative ways.
* **Offline and storage**: allowing webpages to store data on the client-side locally and operate offline more efficiently.
* **Multimedia**: making video and audio first-class citizens in the Open Web.
* **2D/3D graphics and effects**: allowing a much more diverse range of presentation options.
* **Performance and integration**: providing greater speed optimization and better usage of computer hardware.
* **Device access**: allowing for the usage of various input and output devices.
* **Styling**: letting authors write more sophisticated themes.

## Q. ***Describe the difference between a `cookie`, `sessionStorage` and `localStorage`?***

**localStorage:** localStorage is a way to store data on the client’s computer. It allows the saving of key/value pairs in a web browser and it stores data with no expiration date. localStorage can only be accessed via JavaScript, and HTML5. However, the user has the ability to clear the browser data/cache to erase all localStorage data.

**SessionStorage:**  stores data only for a session, meaning that the data is stored until the browser (or tab) is closed.

**cookie:** Stores data that has to be sent back to the server with subsequent XHR requests. Its expiration varies based on the type and the expiration duration can be set from either server-side or client-side .

|                                        | `cookie`                                                 | `localStorage` | `sessionStorage` |
| -------------------------------------- | -------------------------------------------------------- | -------------- | ---------------- |
| Initiator                              | Client or server. Server can use `Set-Cookie` header     | Client         | Client           |
| Expiry                                 | Manually set                                             | Forever        | On tab close     |
| Persistent across browser sessions     | Depends on whether expiration is set                     | Yes            | No               |
| Sent to server with every HTTP request | Cookies are automatically being sent via `Cookie` header | No             | No               |
| Capacity (per domain)                  | 4kb                                                      | 5MB            | 5MB              |
| Accessibility                          | Any window                                               | Any window     | Same tab         |


*Note: If the user decides to clear browsing data via whatever mechanism provided by the browser, this will clear out any `cookie`, `localStorage`, or `sessionStorage` stored. It's important to keep this in mind when designing for local persistance, especially when comparing to alternatives such as server side storing in a database or similar (which of course will persist despite user actions).*

<div align="right">
    <b><a href="#">↥ back to top</a></b>
</div>