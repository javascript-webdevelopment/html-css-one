# HTML / CSS 1

## HTML

HTML stands for Hyper Text Markup Language. It is one of the building block languages of the web that will establish a structure to our web pages. HTML is NOT a programming language, it is a markup language. It does not contain logic and it is used to display and format the elemtents of our web page.

We create an HTML file by ending the name of the file with a `.html` extension. This will tell our browswer and code editors to read the file as HTML. It's important to note that `index.html` is a common name used with the root HTML file since the browser looks for files called `index` by default.

## Syntax Overview

HTML is based around using `tags` to establish an element.

```html
    <tagname>content</tagname>
```

Above we have the basic syntax structure for an HTML tag.

1. We first have the tag itself, the tag uses `<>` angle brackets to delcare that it is an HTML tag.
2. The tag comes in a pair, an opening and closing tag. The closing tag begins with a `</>` to declare that it is ending the HTML tag.
3. Between the angle brackets, is where we will decide what tag we are using.
4. We wrap the tags around the content that we want stored inside that HTML element.

### Basic HTML Structure

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <title>Document</title>
  </head>
  <body>
      <!-- Content of page goes inside the body tag -->
  </body>
</html>
```

Lets breakdown the structure from above:

`<!DOCTYPE html>` - This tag is pretty unique, it's not an HTML element, it's more of a declaration to the browser to inform it what version of HTML we are using. NOTE: it's important to note that this needs to be the very first tag in our HTML file.

`<html>` - The html tag tells the browser that everything inside should be read as html and will act as the root tag for our file. (meaning everything will go in here). We have also added an attribute to the tag to declare what language we are using. We will talk about attributes later on in the notes.

`<head>` - The head tag is a container used to contain metadeta (data about data). Metadata usually defines the title of the document, character set, etyc. Metadata is not displayed to the web page.

`<title>` - This is a metadata tag that will provide the title of our document.

`body` - The body tag is the container for all the elements that will make up our web page. Everything inside of our body tag will be displayed to the web page. This is where we will store our elements such as divs, spans, hyperlinks, text, etc.

### Comments In HTML

We can write comments in our code to help clarify things in the development environment. Comments will not appear in the browser.

We will begin a comment with `<!--` and end the comment with `-->`.

```html
<body>
    <!-- This is a comment and will not be parsed to the browser -->
</body>
```

### Common Tags In HTML

There are many different tags that we can use to creat HTML elements. Here, we will go over a few the most commonly used tags to create the structure of our application.

#### Heading Tags

Header tags are used to declare that the content inside of the brackets are going to be headers for a section on our web page.

There are 6 different header tags that are available to us. The lower the number for the tag, the more important of a header it is.

```html
<h1>Heading One</h1>
<h2>Heading Two</h2>
<h3>Heading Three</h3>
<h4>Heading Four</h4>
<h5>Heading Five</h5>
<h6>Heading Six</h6>
```

#### Paragraph Tags

The `<p>` tag can be used to declare that this element will be a paragraph.

```html
<p>Hey, I'm a paragraph!</p>
```

#### Div Tags

The `<div>` tag represents a division or a section within our web page. This tag is often used as a container to house multiple elements to apply specific styling or functionality using javascript.

```html
<div>
    <p>I'm using a div tag to create a division within my web page to house a paragraph tag</p>
</div>
```

#### Span Tags

The `<span>` tag is used to group inline-element in our document. The span tag does not apply any visual changes to our how structure of elements.

We also use span tags as `hooks` inside of our text to apply specific styling or functionality to a word in our text.

```html
<span>
    <p>I'm a <span>paragraph</span> tag inside of a span!
</span>
```

### Inline Level VS Block Level Elements

Every HTML element has a default display value depending on what tag is used. The two display values are: `inline` and `block`.

#### Block Level

Block level elements always start on a new line and will take up the full width available. (stretches from left to right as much as it can).

For example: the `<div>` element has a `block` display by default.

Other common elements that have a `block` display by default:

* <ul>
* <form>
* <main>
* <footer>
* <nav>

#### Inline Level

Inline level elements *DOES NOT* start on a new line and will only take up as much width as needed.

For example: the `<span>` tag is a common `inline` display element.

Other common elements that have an `inline` display by default:

* <button>
* <a>
* <label>
* <br>

### Tag Attributes

Attributes are used in HTML to provide extra information to a tag. All tags can have attriubutes and will always be placed in the opening or start tag.

Basic Syntax for an attribute:

```html
<tagname attributeName="attributeValue">content</tagname>
```

1. The attribute has a name and a value, the value is set to the name and is wrapped in quotes
2. The attribute is set on the opening tag
3. Attributes use a key/value pairs

Common attributes:

* `href` - the href attribute is commonly paired with an `a` tag and declares the URL to link to
* `src` - image tags commonly use the src tag to determine the source or file name of the image being shown
* `height` - height is another common one used with image tags to determine the height of the image
* `width` - width is another one commonly used with image tags to determine the width of an image

### Seperation Tags

There are tags we can use to create a seperation between our elements. The tags we can use are `<hr>` and `<hr>`.

* `<hr>` - this tag is used to create white space between elements
* `<br>` - this tag is used to create an actual line to split the elements

### Lists

There are two kind of lists we can create in HTML, the ordered and unordered list.

`<ul>` - this is the tag used to create an unordered list
* This will create a list like structure using bullet poiints

`<ol>` - this is the tag used to create an ordered list
* This will create a list like structure using numbers

`<li>` - this is the tag wqe will use to declare the content is a part of a list. It is short for `list item`

Syntax:

```html
<!-- Unordered List -->
<ul>
    <li>About</li>
    <li>Contact</li>
</ul>

<!-- Ordered List -->
<ol>
    <li>About</li>
    <li>Contact</li>
</ol>
```

### Input

Input boxes are way we can capture user input. We can use an `<input>` tag to create the input elements in our HTML.

Input tags will need a `type` attribute applied in order to know what kind of input field we should use. If there is not one applied, it will default to `type="text"` which is just a normal input box a user can type in.

### Buttons

Buttons are a great way to prompt a user to interact and perform an action on your web page.

`<button>` - this is the tag we can use to create a button.

We will need to implement javascript to create the functionality of the button

```html
<button>Cool Button!</button>
```

### Images

We can embed images into our web page by using the `<img>` tag.

We need to apply the `src` attribute to determine what image to show.

Images also use an `alt` attribute to determine what text to show if that image is unavailable.

```html
<img src="images/dog.png" alt="cute puppy" height="500" width="500">
```