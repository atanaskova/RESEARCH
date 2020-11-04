# Document Object Model (DOM)

## Introduction

The Document Object Model (DOM) is a programming API for HTML and XML documents. It defines the logical structure of documents and the way a document is accessed and manipulated. In the DOM specification, the term "document" is used in the broad sense - increasingly, XML is being used as a way of representing many different kinds of information that may be stored in diverse systems, and much of this would traditionally be seen as data rather than as documents. Nevertheless, XML presents this data as documents, and the DOM may be used to manage this data.


With the Document Object Model, programmers can create and build documents, navigate their structure, and add, modify, or delete elements and content. Anything found in an HTML or XML document can be accessed, changed, deleted, or added using the Document Object Model, with a few exceptions - in particular, the DOM interfaces for the internal subset and external subset have not yet been specified.


As a W3C (World Wide Web Consortium) specification, one important objective for the Document Object Model is to provide a standard programming interface that can be used in a wide variety of environments and applications. The Document Object Model can be used with any programming language. 


**The DOM defines a standard for accessing documents:**


*The W3C Document Object Model (DOM) is a platform and language-neutral interface that allows programs and scripts to dynamically access and update the content, structure, and style of a document.*

Understanding the DOM is a must for anyone working with HTML or XML.

The name "Document Object Model" was chosen because it is an "object model" is used in the traditional object oriented design sense: documents are modeled using objects, and the model encompasses not only the structure of a document, but also the behavior of a document and the objects of which it is composed.

As an object model, the Document Object Model identifies:


- the interfaces and objects used to represent and manipulate a document
- the semantics of these interfaces and objects - including both behavior and attributes
- the relationships and collaborations among these interfaces and objects

The W3C DOM standard is separated into 3 different parts:


- Core DOM - standard model for all document types
- XML DOM - standard model for XML documents
- HTML DOM - standard model for HTML documents

## What is the Core DOM?

This specification defines a minimal set of objects and interfaces for accessing and manipulating document objects. The functionality specified in this draft (the core functionality) should be sufficient to implement higher level operations, such as navigating and modifying a document.


Level 1 of the Document Object Model (DOM) provides a common API for software developers and web script authors to access and manipulate parsed HTML and XML content inside conforming products. Primary document structures and some document type declarations are made available. Level 1 also allows creation from scratch of entire web documents in memory, saving those documents persistently is left to the programmer. DOM Level 1 is intentionally limited in scope to methods to represent and manipulate document structure and content, a standard API for controlling how documents are rendered via stylesheets, validated against a DTD, accessed by given users, etc., will be specified in a subsequent revision level of the DOM.

For more information about:


1. Fundamental Interfaces
2. Extended Interfaces

[Click Here!](https://www.w3.org/TR/WD-DOM/level-one-core.html)

## What is the XML DOM?


The XML DOM is:

- A standard object model for XML
- A standard programming interface for XML
- Platform- and language-independent
- A W3C standard


In other words: The XML DOM is a standard for how to get, change, add, or delete XML elements.


The DOM models XML as a set of node objects. The nodes can be accessed with JavaScript or other programming languages.


The programming interface to the DOM is defined by a set standard properties and methods.


**Properties** are often referred to as something that is.

**Methods** are often referred to as something that is done.

The XML DOM defines a standard way for accessing and manipulating XML documents. It presents an XML document as a tree-structure.

According to the XML DOM, everything in an XML document is a node:

- The entire document is a document node
- Every XML element is an element node
- The text in the XML elements are text nodes
- Every attribute is an attribute node
- Comments are comment nodes

```xml
<?xml version="1.0" encoding="UTF-8"?>
    <bookstore>
        <book category="cooking">
            <title lang="en">Everyday Italian</title>
            <author>Giada De Laurentiis</author>
            <year>2005</year>
            <price>30.00</price>
        </book>
        <book category="children">
            <title lang="en">Harry Potter</title>
            <author>J K. Rowling</author>
            <year>2005</year>
            <price>29.99</price>
        </book>
        <book category="web">
            <title lang="en">XQuery Kick Start</title>
            <author>James McGovern</author>
            <author>Per Bothner</author>
            <author>Kurt Cagle</author>
            <author>James Linn</author>
            <author>Vaidyanathan Nagarajan</author>
            <year>2003</year>
            <price>49.99</price>
        </book>
        <book category="web" cover="paperback">
            <title lang="en">Learning XML</title>
            <author>Erik T. Ray</author>
            <year>2003</year>
            <price>39.95</price>
        </book>
    </bookstore>

```
All nodes can be accessed through the tree. Their contents can be modified or deleted, and new elements can be created.

The node tree shows the set of nodes, and the connections between them. The tree starts at the root node and branches out to the text nodes at the lowest level of the tree:


![alt text](https://www.w3schools.com/xml/nodetree.gif)

>DOM representation of the XML file


## What is the HTML DOM?

The HTML DOM is a standard **object** model and **programming interface** for HTML. It defines:

- The HTML elements as **objects**
- The **properties** of all HTML elements
- The **methods** to access all HTML elements
- The **events** for all HTML elements


In other words: **The HTML DOM is a standard for how to get, change, add, or delete HTML elements.**

When a web page is loaded, the browser creates a **D**ocument **O**bject **M**odel of the page.

The HTML DOM model is constructed as a tree of Objects.

For instance, consider this table, taken from an HTML document:

```html
<table>
    <tbody> 
        <tr> 
            <td>Shady Grove</td>
            <td>Aeolian</td> 
        </tr> 
        <tr>
            <td>Over the River, Charlie</td>
            <td>Dorian</td> 
        </tr> 
    </tbody>
</table>
```

The Document Object Model represents this table like this:

![alt text](https://www.w3.org/TR/WD-DOM/table.gif)

>DOM representation of the HTML file


The goals of the HTML-specific DOM specification are:

- to specialize and add functionality that relates specifically to HTML documents and elements.
- to address issues of backwards compatibility with the Level 0 Document Object Model.
- to provide convenience mechanisms, where appropriate, for common and frequent operations on HTML documents.


The key differences between the core DOM and the HTML application of DOM is that the HTML Document Object Model exposes a number of convenience methods and properties that are consistent with the existing models and are more appropriate to script writers.