# CSS Documentation 

## Introduction
CSS (Cascading Style Sheets) is a style sheet language used to describe the presentation of a document written in HTML. It defines how elements should be rendered on screen, paper, or in other media.


## CSS Syntax
CSS follows a specific syntax where styles are applied to elements using **selectors** and **declaration blocks**. The declaration block contains **properties** and **values** which define the styles for the elements.

---

## Including CSS in HTML
There are three ways to incorporate CSS into an HTML document:

1. **Inline CSS**: Applies CSS directly within an HTML element's `style` attribute.
2. **Internal CSS**: Embedded in the HTML file using the `<style>` tag inside the `<head>`.
3. **External CSS**: Linked as a separate `.css` file using the `<link>` tag.

---

## Color Properties
CSS provides properties to manipulate the color of elements:

- **color**: Sets the foreground (text) color.
- **background-color**: Defines the background color of an element.
- **Color Formats**: Can be defined using named colors, RGB values, hexadecimal codes

---

## CSS Selectors
CSS selectors are used to target HTML elements for styling:

- **Universal Selector (`*`)**: Selects all elements in the document.
- **Element Selector**: Selects all instances of a specific HTML element.
- **ID Selector (`#id`)**: Targets a single element with a specific `id` attribute.
- **Class Selector (`.class`)**: Targets elements with a specific `class` attribute.

---

## Text Properties
CSS provides a set of properties to control the appearance of text:

- **text-align**: Specifies horizontal alignment of text within an element.
- **font-weight**: Determines the thickness or boldness of the text.
- **text-decoration**: Adds effects like underline, overline, or strikethrough to text.
- **font-family**: Sets the typeface or font family for the text.
- **text-transform**: Controls capitalization and transformation of text.
- **line-height**: Defines the space between lines of text.
- **font-size**: Specifies the size of the text.

---

## Box Model
The **CSS Box Model** is a box that wraps around every HTML element. It consists of the following properties:

- **Content**: The actual content inside the box (text, images, etc.).
- **Padding**: Clears an area around the content (inside the border) 
- **Border**: Surrounds the padding and content.
- **Margin**: Clears an area outside the border.
  

  * Atribute related to Content
    - `Width`
    - `Height`
  * Atributes related to padding
    - `padding-left`
    - `padding-right`
    - `padding-top`
    - `padding-bottom`
    - `padding`: top,right,bottom,left
  * Atributes related to margin
    - margin-left
    - margin-right
    - margin-top
    - margin-bottom
    - margin : top,right,bottom,left
  * Atribute related to Broder
    - Border-width
    - Baroder-style: solid/dotted/dash
    - Border-color
    - Border: width style color
    - Border-radius: 

The Box Model determines the element’s dimensions and space between elements.

---

## Display Properties
The **display** property controls how an element is displayed on the web page. Common display values include:

- **block**: The element takes up the entire width available, with a line break before and after.
- **inline**: The element takes up only as much width as it needs, without breaking the line.
- **inline-block**: Similar to `inline`, but allows setting `width` and `height`.
- **none**: The element is not displayed (removed from the document flow).

---

## Visibility
The **visibility** property determines whether an element is visible or hidden, while still occupying space in the layout.

- **visible**: The element is visible (default).
- **hidden**: The element is hidden, but space is still reserved.

## Positioning

### Position Property
The position CSS property defines how an element is positioned in the document. Common values include:

* static: The default positioning. The top, right, bottom, left, and z-index properties have no effect.
* relative: The element is positioned relative to its original position. The top, right, bottom, left, and z-index properties will work.
* absolute: Positioned relative to the nearest positioned ancestor. The element is removed from the document flow.
* fixed: Positioned relative to the browser window, staying in place when the page is scrolled.
* sticky: Positioned based on the user's scroll position.

## Background Image :
Used to set an image as background
* background-image : url("image.jpeg");
* background-size : cover / contain / auto

## Flexbox
Flexible Box Layout: It is a one-dimensional layout method for arranging items in rows or columns.
#### The Flex Model
##### Flexbox Direction: It sets how flex items are placed in the flex container, along which axis and direction.
* flex-direction : row; (default)
* flex-direction : row-reverse;
* flex-direction : column;
* flex-direction : column-reverse;

#### Flex Properties: for Flex Container
* justify-content : alignment along the main axis(flex-start / flex-end / centre /space-evenly)
* flex-wrap : nowrap / wrap / wrap-reverse 
* align-items : alignment along the cross axis.
* align-content : alignment of space between & around the content along cross-axis

#### Flex Properties
* align-self : alignment of individual along the cross axis.space is available
* flex-grow : how much a flex item will grow relative to the rest of the flex items if
* flex-shrink : how much a flex item will shrink relative to the rest of the flex items if space is available

 #### Media Queries
 - Help create responsive websites for various screen sizes and orientations.
 - Examples:
   ```css
   @media (max-width: 600px) {
       div { background-color: red; }
    }
   @media (min-width: 600px) {
       div { background-color: blue; }
   }
   ```
 - Ensure layouts look good on devices like laptops, phones, tablets, etc.

#### Transitions
 - Define changes between element states smoothly.
 - Key properties:
   - `transition-property`: e.g., font-size, width.
   - `transition-duration`: e.g., 2s, 400ms.
   - `transition-timing-function`: e.g., ease-in, linear.
   - `transition-delay`: e.g., 0.2s.

#### CSS Transforms
 - Apply 2D/3D transformations:
   - **Rotate**: `transform: rotate(45deg);`
   - **Scale**: `transform: scale(2);`
   - **Translate**: `transform: translate(20px, 50px);`
   - **Skew**: `transform: skew(30deg);`
#### PSEUDO CLASS
1. `:hover` - Selects links or elements when the mouse hovers over them. It's widely used for styling interactive elements like buttons and links.
2. `:active` - Selects an element when it is being activated (e.g., when a link is clicked). It is often used for styling the click state of buttons and links.
3. `:focus` - Selects an element (like an input) when it has focus, commonly used to style form fields or interactive elements for accessibility.
4. `:visited` - Selects all links that have been visited by the user, allowing for different styling based on the link state.
5. `:first-child` - Selects the first child of a parent element, often used for styling the first item in a list or section differently.

#### Animation
* To animate CSS elements

```
 @keyframe myName {
from { font-size : 20px; } to { font-size : 40px; }
}
```
* Animation Properties
`animation-name`
`animation-duration`
`nimation-timing-function`
`animation-delay`
`animation-iteration-count`
`animation-direction`

* Animation Shorthand

- animation : myName 2s linear 3s infinite normal

* % in Animation
```
@keyframe myName {
0% { font-size : 20px; }
50% { font-size : 30px; }
100% { font-size : 40px; }
}
```

---
---
---
---
---



### PROJECT 01
##### PROBLEM STATEMENT
1. Create a simple div with an id "box".
* Add some text content inside the div.
* Set its background color to blue.
2. Create 3 headings with h1, h2 & h3.
* Give them all a class "heading" & set color of "heading" to red.
3. Create a button & set its background color to :
* green using css stylesheet
* blue using <style> tag
* pink using inline style
### PROJECT 02
##### PROBLEM STATEMENT
1. Create a heading centred on the page with all of its text capitalized by default.

2. Set the font family of all the content in the document to "Times New Roman".

3. Create one div inside another div.
* Set id & text "outer" for the first one & "inner" for the second one.
* Set the outer div text size to 25px & inner div text size to 10px.
### PROJECT 03
##### PROBLEM STATEMENT
* Create a div with height & width of 100px.
* Set its background color to green & the border radius to 50%.
* Create the following navbar.
  `amazon.in  Account Mycart Contactus  Searchbar Searchbutton`
 

### PROJECT 04
##### PROBLEM STATEMENT
* Create a webpage layout with a header, a footer & a content area containing 3 divs.
Set the height & width of divs to 100px.
(add the previous navbar in the header)
* Add borders to all the divs.
* Give the content area an appropriate height.

### LABSHEET 05
##### PROBLEM STATEMENT
* Createthefollowinglayoutusingthegivenhtml.
* Give the div a height, width & some background image.
* Use z-index to place the div on top of page.
* Use the appropriate position property for the div element to place it at the right end of the page. (The div should not move even on scroll)


### PROJECT 06
##### PROBLEM STATEMENT
* Qs: Create a navbar with 4 options in the form of anchor tags inside list items.Now, use flexbox to place them all spaced equally in a single line.
* Qs: Use flex box to center one div inside another div.
* Qs: Which has higher priority - align-items or align-self?5


### PROJECT 07

* the color of a div changes to green for viewport width less than 300px
* the color of a div changes to pink for width between 300px & 400px the color of a div changes to red for width between 400px & 600px
* the color of a div changes to blue for width above 600px

### PROJECT08
* Qs: Create a simple loader using CSS
* Step1 : create a div with circular shape & a thick border from one end(top/bottom/left/right)
* Step2 : To make it spin create an animation which transforms it from 0deg to 360deg
* Step3 : Add the animation property to the loader with infinite duration
