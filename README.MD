# HTML / CSS 1

## HTML

HTML stands for Hyper Text Markup Language. It is one of the building block languages of the web that will establish a structure to our web pages. HTML is NOT a programming language, it is a markup language. It does not contain logic and it is used to display and format the elemtents of our web page.

We create an HTML file by ending the name of the file with a `.html` extension. This will tell our browswer and code editors to read the file as HTML. It's important to note that `index.html` is a common name used with the root HTML file since the browser looks for files called `index` by default.

### Syntax Overview

HTML is based around using `tags` to establish an element.

```html
    <tagname>content</tagname>
```

Above we have the basic syntax structure for an HTML tag.

1. We first have the tag itself, the tag uses `<>` angle brackets to delcare that it is an HTML tag.
2. The tag comes in a pair, an opening and closing tag. The closing tag begins with a `</>` to declare that it is ending the HTML tag.
3. Between the angle brackets, is where we will decide what tag we are using.
4. We wrap the tags around the content that we want stored inside that HTML element.

Some tags can be self closing or `void`.

```html
    <input />
```

Notice how there is only one tag and it uses a forward slash at the ending of the tag.

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

### MetaTags

Meta tags give overall information about your site that is used by search engines to search and display your website in their page rank algorithim.

Meta tags need to be placed inside the `<head>` tag of your file.

```html
<head>
    <meta charset="UTF-8">
    <!-- charset determines the letter of the alphabet and characters used -->
    <meta name="description" content="best website ever made">
    <!-- the description will show up on a search engine as a primary description -->
    <meta name="keywords" content="cool website me mine this is cool check it out">
    <!-- keyowrds are used to help the search engine recognize what words could help find your site-->
    <meta name="author" content="tayte stokes">
    <!-- author shows who created the website -->
    <meta name="viewport" ontent="width=device-width, initial-scale=1.0">
    <!-- view port will tell the browser what device is using the website and adjust for mobile design -->
</head>
```

### Semantic Markup

Semantic elements are elements that simply provide a meaning to the browser and developer rather than just representation. 

Example of NON-Semantic: <div>, <span>

Example of Semantic: <footer>, <header>, <nav>

Notice how the tags are providng a meaning to what content will be stored between them. Using semantic HTML will help communicate to the browser what your web page is and this will also be communicated to search engines making it easier to find your site.

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

Different types of inputs:

* <input type="button"> 
* <input type="checkbox">
* <input type="color">
* <input type="date">
* <input type="datetime-local">
* <input type="email">
* <input type="file">
* <input type="hidden">
* <input type="image">
* <input type="month">
* <input type="number">
* <input type="password">
* <input type="radio">
* <input type="range">
* <input type="reset">
* <input type="search">
* <input type="submit">
* <input type="tel">
* <input type="text">
* <input type="time">
* <input type="url">

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

### Form

A `<form>` tag can be used to create a form in our HTML. This form can be used to collect user data.

An HTML form contains `form elements`. Form elements are different types of input fields like text area, radio butotns, check boxes, etc.

```html
<form>
  First name:<br>
  <input type="text" name="firstname"><br>
  Last name:<br>
  <input type="text" name="lastname">
  <input type="submit" value="Submit">
</form>
```

`<input type="text">` - this defines a one line input field for user input

`<input type="submit">` - this defines a form button that will submit the data typed into the form

### Tables

We can create tables to organize content in HTML by using a `<table>` tag.
* Every table row is created using the `<tr>` tag.
* A table header column is created using the `<th>` tag
* a table cell is defined using the `<td>` tag

```html
<table>
  <tr>
    <th>Firstname</th>
    <th>Lastname</th> 
  </tr>
  <tr>
    <td>Tayte</td>
    <td>Stokes</td> 
  </tr>
  <tr>
    <td>Matt</td>
    <td>Bodily</td> 
  </tr>
  <tr>
    <td>Catie</td>
    <td>Mondon</td> 
  </tr>
</table>
```

## CSS

CSS stands for cascading style sheets. CSS is another one of the core languages of the web, but CSS is used mainly for creating style and layout of our HTML structure.

CSS is not a programming language, it is a styling language. We can add CSS to our HTML files.

### Methods To Do CSS

There are three main ways that we can do CSS:

1. Inline CSS

This is where we use the `style=""` attribute on the opneing tag of a HTML element.
We should always try to avoid adding css this way

2. Internal CSS

This is where we can write our CSS in the same HTML file, but we encapsulate it inside of a `<style>` tag.

3. External CSS

This is where we create a seperate style sheet to house our styling.

To follow this pattern (which is the most common way to write css) we will need to make a style sheet that ends with the extension `.css`.
Then we will need to link our style sheet to our HTML file. Inside of the `<head>` tag, we can use a `<link>` tag to link them together.

```html
<head>
    <link rel="stylesheet" type="text/css" href="stylesheet.css">
</head>
```

Above there are three attributes associated with the `<link>` tag to link the style sheet:
1. `rel` - this is the attribute where we tell the HTML file what the relation is
2. `type' - this is where we declare the type of file
3. `href` - this is where we declare the path to the style sheet we want to use

### Selectors

Selectors are used in CSS to determine what element we want to apply a specific styling to. Selectors are followed by a set of curly braces that is known as the `declaration`. Inside the declaration, we will use key/value pairs to select a property on the select element and apply value to that property.

```css
div {
    background-color: tomato;
}
```

There are a few ways to select an element to apply styling to:

1. We select the tag, if we do this it will apply this style to all the tags that we have selected

```css
div {
    background-color: tomato;
}
```

2. We can select an html class.

On the html tag, we can give it an attribute of `class=""` to give it a class name. We can use classes to apply styles to multiple elements using that class name.

HTML:
```html
<div class="container">

</div>
```

CSS:
```css
.container {
    background-color: tomato;
}
```

We need to prefix our selector with a `.` to declare we are looking for a class.

3. We can select an html id

This is the same as the selecting a class, but we should never have more thaan one element with the same id.

HTML:
```html
<h1 id="title">This is my title</h1>
```

CSS:
```css
#title {
    color: tomato;
}
```

Notice how we prefix our selector with a `#` to declare we are selecting an id.

### CSS Selector Patterns

We can target multple elements at once, or be very specific about what element to select to apply a set of styles to.

Using these different selector patterns will help keep our code `DRY`.

We can use a `,` to select multiple elements at once to apply the same styling.

```css
h1, div, span {
    color: blue,
    background-color: tomato;
}
```

We can use a white space ` ` or the carot `>` to go select a specific element that is nested inside of other elements.

```css
nav div h1 {
    color: blue
}

nav > div > h1 {
    color: red;
}
```

### CSS Specificty

CSS specificity refers to a set of rules that browsers use to determine which styles are applied when there is a conflict. 

This set of rules work of a point system. Each select has a different point value given to it. The higher the point value, the more likely that style is to be applied to the element. We use this set of rules to determine how to can override or avoid overriding styles that conflict.

Point System:

`Inline Styling` - this is where we apply styles directly to the HTML tag. Inline styling is worth 1000 points.

```html
<h1 style="color: blue">This is my title</h1>
```

`ID` - when we use an id to apply styles, it will gain 100 points in this system

```css
#title {
    color: blue
}
```

`Class` - when a class is selected to apply an element, it gains 10 points

```css
.containers {
    background-color: tomato;
}
```

`element` - when we target an element directly using this tag, it is applied only 1 point

```css
div {
    background-color: tomato;
}
```

### DRY CSS

`DRY` stands for 'dont repeat yourself'. This is a practice to follow to help us avoid writing the same code multple times.

Practices to help follow the DRY pattern:

- Use classes to style many elements
- Style as generally as you can, then make any adjustments for specific styling
- Semantic HTML can help you name elements even more precise

### Reset CSS

By default, the browser will apply it's own set of styling rules to the elements inside of an HTML file.

We can use a `reset css` file to remove all default styling from a browser.

Check this website out to get a prebuilt reset css file: ![reset css](https://meyerweb.com/eric/tools/css/reset/)

### Display Property

The `display` property is a property can help aid us in setting up the lay out for each element.

`display` has multiple values that we can give it:

`block` - this display value will cause each element to appear own a new line and will take up the full amount of width that it can

`inline` - this value will cause each element to not go to a new line and will only take up as much width as it needs. You can not edit the height or width of an inline element.

`inline-block` - works just like inline, but allows us to edit the height and width of the element

### Floats

The `float` property places an element on the left or right side of it's container, allowing text and inline elements to wrap around it.

```css
div {
    float: left;
}

img {
    float: right;
}
```

`clear` is the property we can use if we want to declare that nothing can sit on the side of the floated element

```css
div {
    float: right;
}

h1 {
    clear: right;
    /* this will make the h1 sit underneath the div because we are clearing everything to the left side of the div positioned right */
}
```

### Text Properties

There are multiple properties we can use to manipulate the way text looks on our web page.

Using good fonts and text colors are important for good design.

There are many different properties we can modify:

`font-size` - this will change the size of the font

`color` - this will change the color of the text inside of an element

`line-height` - will determine the total amount of space the content height will take up

`text-align` - property that defines where to align the text according to the size of the element

`font-family` - will determine what font family we want our text to be in

`letter-spacing` - will determine how much white space should be bewtween each character

### Background Properties

These are properties that we can use to modify the background of an element.

There are many different background properties we can modify:

`background-image` - we can use an image as a background for an element. The content inside of the element will appear above the image.

```css
div {
    background-image: url('image.png')
}
```

`background-size` - this determines the size of the background

`background-position` - we can use this to adjust where and how the background image will align

`background-repeat` - we can use this to choose how and if the background image should be repeated

`background-color` - we can use this to change the color of a background on an element

### Box Model

The box model is a tool we can use when it comes to styling the layout of our elements. The box model is more of a concept or pattern to follow rather than actual code values.

Following the box model means that we are looking to style four specific parts of our elements in order to get the right layout and design of the element.

Those four properties are:

1. Margin
Margin is the white space between each element

2. Border
Border is the border of the box

3. Padding
Padding is the white space between the content of an element and it's border

4. Content
The content of an element is anything inside of an element such as text, images, etc.