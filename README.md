## CSS documentation

### 1.1 Introduction to CSS

- CSS stands for Cascading Style Sheets
- It is used to style html elements
- Initial release on December 17, 1996
- 3 main ways to add css with html: Inline CSS, Internal CSS, External CSS

  - Inline CSS

    - Inline CSS refers to style inside html element. Syntax: `<tagName style="property:value; property:value; ... ">`
    - Inline CSS Example is given below:

      ```css
      <h1 style="background-color: green">Welcome to CSS</h1>
      <p style="color: red; text-align: center;">Welcome to css</p>
      ```

  - Internal CSS

    - Inside `<head>` tag we can use internal css with the help of `<style>` tag
    -  Internal CSS Example is given below:   

        ```css
        <style>
            div {
                padding: 10px;
                text-align: center;
                font-weight: 500;
            }
        </style>
        ```
  - Exetrnal CSS

    - Inside `<head>` tag we can link the external css file with the help of `<link rel="stylesheet" href="cssFileNameOrAddressHere"/>` tag
    - create a css file with an extension of .css as shown below: style.css

      ```css
      p {
        background-color: green;
        color: white;
      }
      ```

    - then add the css file inside html file as shown below:

      ```html
      <head>
        <title>Learn Internal CSS</title>
        <link rel="stylesheet" href="style.css"/>
      </head>
      <body>
        <p>Welcome to CSS</p>
        <p>aperiam fugiat blanditiis voluptatibus quo!</p>
      </body>
      ```

### 1.2 Basic Selectors

- Basic Selectors: Element Selector, grouping selectors, nested selector, Universal Selector, ID selectors, class selectors

- Element selector: select an element by using its name.   
Example:

  ```css
  h1 {
      background-color: green;
  }
  ```

- Grouping selector: select multiple element by using their names separted with comma.  
Example:

  ```css
  h1, h2, p {
      background-color: green;
  }
  ```

- Nested selector: select elements by nesting. ul li a {...}, div p {...}.    
Example:

  ```css
  ul li a {
    color: red;
    text-decoration: none;
  }
  ```

- Universal selector can help to select all the html elements. It is denoted by *   
Example:

  ```css
  * {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
  }
  ```

- id selector: is unique inside html document. #id can help to select any element with a given id. use # notation for selecting an id. Example:

  ```css
  #para {
    text-align: center;
  }
  ```

- class selector: .class can help to select any element with a given class. use dot notation for selecting a class.   
Example:

  ```css
  .myDiv {
    font-size: 20px;
  }
  ```

### 1.3 Pseudo class & Pseudo element

- Pseudo class selectors

  - Link Pseudo classes: link, visited, hover, active
  - Input Pseudo classes: focus, enabled, disabled, checked, required, optional, valid, invalid
  - General Pseudo classes: first-child, last-child, first-of-type, last-of-type, nth-child(n), nth-last-child(n), nth-last-of-type(n), root, not
  - References: https://developer.mozilla.org/en-US/docs/Web/CSS/Pseudo-classes
  - syntax for Pseudo class selectors

    ```css
    selector:pseudo-class {
        property: value;
    }
    a:hover{
        color: blue;
    }
    ```

- Pseudo element selectors

  - Common Pseudo element: after, before, first-letter, first-line, placeholder, select
  - References: https://developer.mozilla.org/en-US/docs/Web/CSS/Pseudo-elements
  - syntax for Pseudo element selectors

    ```css
    selector::pseudo-element {
        property: value;
    }
    h1::after {
        content: url(smiley.gif);
    }
    ```

### 1.4 Font Properties, Color, Text styling, icons

- font-family, font-style, font-weight, font-variant, font-size, line-height

  ```css
  p {
    font-size: 18px;
    font-weight: 500;
    font-style: oblique;
    font-variant: normal;
    font-family: 'Times New Roman', Times, serif;
  }
  ```

- Color Important Tools:

  - Canva color wheel: https://www.canva.com/colors/color-wheel/
  - Color Picker: https://htmlcolorcodes.com/color-picker/
  - Image color picker: https://imagecolorpicker.com/en
  - How to use colorzilla plugin, how to use https://flatuicolors.com/

    ```css
    p {
        color: red;
        color: rgb(0, 255, 0);
        color: #ffda77;
    }
    ```

- Text styling properties:

  - text-align, text-transform, text-decoration, text-shadow, text-indent, letter-spacing, word-spacing, line-height

    ```css
    p {
    text-align: center;
    text-transform: capitalize;
    text-decoration: dotted;
    text-shadow: 2px 2px green;
    text-shadow: 2px orange;
    text-indent: 50px;
    letter-spacing: 2px;
    line-height: 0.8;
    word-spacing: 2px;
    }
    ```

- How to use font awesome icons

  - get font awesome icons here: https://fontawesome.com/
  - get font awesome cdn from here: https://cdnjs.com/libraries/font-awesome
  - add the font awesome cdn inside the html head tag and then you are ready to use font awesome icons   

    ```css
    <i class="far fa-address-card"></i>
    <i style="color: red;" class="far fa-address-card fa-2x"></i>
    ```

### 1.5 Comments

- Comments are used to explain the code.
- Comment may help when you edit the source code at a later date.
- Comments are ignored by browsers.
- start with a forward slash and asterisk ( /* ), and you end the comment it with an asterisk and forward slash ( */ ).
- CSS has two types of comment.

  - Single line comment

    ```css
    /* This is a single-line comment */
    ```

  - Multiple line comment

    ```css
    /* This is
    a multi-line
    comment */
    ```

### 1.6 Box Model

- Margin

  - margin-top, margin-right, margin-bottom, margin-left
  - margin

- Padding

  - padding-top, padding-right, padding-bottom, padding-left
  - pdding

- border

  - border-top, border-right, border-bottom, border-left
  - border: borderWidth borderColor borderStyle;
    
    ```css
    p {
      border: 3px solid black;
    }
    ```

- box-sizing: border-box
- opacity: value; value can be between 0-1
- display: inline/block
- overflow: value; here default value is visible, hidden, auto, scroll

### 1.7 Background

- How to set background image in webpage

  - background-image, background-position, background-size, background-repeat

    ```css
    body {
      background-image: url("./images/me.JPG");
      background-size: cover;
      background-repeat: no-repeat;
      height: 100vh;
      background-position: center;
    }
    ```

- background: linear-gradient(direction, colors)

  ```css
  .banner {
    width: 400px;
    height: 400px;
    background: linear-gradient(to right, green, orange);
  }
  ```

### 1.8 CSS Layout - float and clear

- float: left/right
- clear: left/right/both
- example: create 3 div in html and add div1, div2, div3 classes with them

  ```css
  .div1 {
    width: 50%;
    height: 10rem;
    background-color: orange;
    float: left;
  }
  .div2 {
    width: 50%;
    height: 10rem;
    background-color: plum;
    float: left;
  }
  .clear-div {
    clear: both;
  }
  .div3 {
    height: 10rem;
    background-color: burlywood;
  }
  ```

### 1.9 CSS Layout - Position and z-index

- `position: static(default)/absolute/relative/fixed/sticky`
- make sure to use top, right, bottom, left property with position property
- `z-index: value;` value can be negative or positive  
Example:

  ```html
  <body>
    <h1>This is a heading</h1>
    <img src="img_tree.png">
    <p>Because the image has a z-index of -1, it will be placed behind the text.</p>
  </body>
  ```
  ```css
  img {
    position: absolute;
    left: 0px;
    top: 0px;
    z-index: -1;
  }
  ```

### 2.0 CSS Layout : Flexbox properties

- flex-direction, flex-wrap, justify-content, align-items, flex-grow, flex-shrink

  ```CSS
  .container {
    display: flex; /* or inline-flex */
  }
  ```

  - flex-direction
   
     - row (default): left to right in ltr; right to left in rtl
     - row-reverse: right to left in ltr; left to right in rtl
     - column: same as row but top to bottom
     - column-reverse: same as row-reverse but bottom to top

        ```css
        .container {
            flex-direction: row | row-reverse | column | column-reverse;
        }
        ```

  - flex-wrap

    - nowrap (default): all flex items will be on one line
    - wrap: flex items will wrap onto multiple lines, from top to bottom.
    - wrap-reverse: flex items will wrap onto multiple lines from bottom to top.
    
        ```css
        .container {
            flex-wrap: nowrap | wrap | wrap-reverse;
        }
        ```

  - justify-content

    - flex-start (default): items are packed toward the start of the flex-direction.
    - flex-end: items are packed toward the end of the flex-direction.
    - center: items are centered along the line
    - space-between: items are evenly distributed in the line; first item is on    the start line, last item on the end line
    - space-around: items are evenly distributed in the line with equal space around them. Note that visually the spaces aren???t equal, since all the items have equal space on both sides. The first item will have one unit of space against the container edge, but two units of space between the next item because that next item has its own spacing that applies.
    - space-evenly: items are distributed so that the spacing between any two items (and the space to the edges) is equal.

      ```css
        .container {
            justify-content: flex-start | flex-end | center | space-between | space-around | space-evenly;
        }
      ```
  - align-items

    - stretch (default): stretch to fill the container (still respect min-width/max-width)
    - flex-start: items are placed at the start of the cross axis.
    - flex-end: items are placed at the end of the cross axis.
    - center: items are centered in the cross-axis.
    - baseline: items are aligned such as their baselines align

        ```css
        .container {
            align-items: stretch | flex-start | flex-end | center | baseline;
        }
        ```

### 2.1 CSS Layout :  Grid

- grid-template-columns, grid-template-rows, grid-gap, grid-column, grid-row

  - grid-template-columns

    ```css
    .grid-container {
        display: grid;
        grid-template-columns: auto auto auto auto;
        grid-template-columns: 250px 250px 250px 250px;
        grid-template-columns: 1fr 1fr 1fr 1fr;
        grid-template-columns: repeat(4,25%);
        grid-template-columns: repeat(4,1fr);
        grid-template-columns: repeat(auto-fit, minmax(250px,1fr));
    }
    ```

  - grid-gap

    ```CSS 
    .grid-container {
        display: grid;
        /* grid-gap: grid-row-gap grid-column-gap; */
        grid-gap: 20px 20px;
        /* grid-row-gap: length; */
        grid-row-gap: 20px;
        grid-column-gap: 20px;
    }
    ```

  - grid-column

    ```css
    .grid-container {
        display: grid;
    }
    .grid-item {
        grid-column: 1 / 3;
        grid-column: 1 / span 3;
        grid-column-start: 1;
        grid-column-end: 3;
    }
    ```

  - grid-template-areas

    ```css
    .item1 { grid-area: header; }
    .item2 { grid-area: menu; }
    .item3 { grid-area: main; }
    .item4 { grid-area: right; }
    .item5 { grid-area: footer; }

    .grid-container {
    grid-template-areas:
        'header header header header header header'
        'menu main main main right right'
        'menu footer footer footer footer footer';
    }
    ```

### 2.2 text-shadow and box-shadow

- text-shadow: x-value y-value blur-value color
- box-shadow: x-value y-value color
- box-shadow: x-value y-value blur-radius color
- box-shadow: inset x-value y-value color

  ```css
  h1 {
    text-shadow: 2px 2px 8px #FF0000;
  }
  .myDiv {
    box-shadow: 10px 10px 8px #888888;
  }
  ```

### 2.3 CSS Transforms, Transitions, Animations

- 2D Transforms - translate(x,y) , scale(x, y) , rotate(angle) , skew(angle)
- 3D Transforms - rotateX(angle) , rotateY(angle) , rotateZ(angle)

  | Function | Description |
  | ------ | ------ |
  | translate(x,y) | Defines a 2D translation, moving the element along the X- and the Y-axis |
  | scale(x,y) | Defines a 2D scale transformation, changing the elements width and height |
  | rotate(angle) | 	Defines a 2D rotation, the angle is specified in the parameter |
  | skew(x-angle,y-angle) | Defines a 2D skew transformation along the X- and the Y-axis |
  | rotateX(angle) | 	Defines a 3D rotation along the X-axis |
  | rotateY(angle) | 	Defines a 3D rotation along the Y-axis |
  | rotateZ(angle) | Defines a 3D rotation along the Z-axis |

  - __Note :__ The translate() method moves an element from its current position
  - __Note :__ The scale() method increases or decreases the size of an element
  - __Note :__ The skew() method skews an element into a given angle.
  - __Note :__ The rotate() method rotates an element clockwise or counter-clockwise.

    ```css
    .div1:hover {
      transform: rotate(-120deg);
    }
    .div2:hover {
      transform: scale(2,-2);
    }
    .div3:hover {
      transform: translate(50px, 100px);
    }
    .div4.hover {
      transform: scale(2, 3);
    }
    ```

- Transitions 

  | Property | Description |
  | ------ | ------ |
  | transition | A shorthand property for setting the four transition properties into a single property |
  | transition-delay | Specifies a delay (in seconds) for the transition effect |
  | transition-duration | Specifies how many seconds or milliseconds a transition effect takes to complete |
  | transition-property | Specifies the name of the CSS property the transition effect is for |
  | transition-timing-function | 	Specifies the speed curve of the transition effect |

  ```css
  div {
    transition-property: width;
    transition-duration: 2s;
    transition-timing-function: linear;
    transition-delay: 1s;
  }
  ```

- Animations properties

  - @keyframes
  - animation-name
  - animation-duration
  - animation-delay
  - animation-iteration-count
  - animation-direction
  - animation-timing-function
  - animation-fill-mode
  - animation  

    ```html
    <html>
      <head>
        <title>Document</title>
        <style> 
          div {
            width: 100px;
            height: 100px;
            background-color: red;
            position: relative;
            animation-name: example;
            animation-duration: 5s;
            animation-timing-function: linear;
            animation-delay: 2s;
            animation-iteration-count: infinite;
            animation-direction: alternate;
          }

          @keyframes example {
            0%   {background-color:red; left:0px; top:0px;}
            25%  {background-color:yellow; left:200px; top:0px;}
            50%  {background-color:blue; left:200px; top:200px;}
            75%  {background-color:green; left:0px; top:200px;}
            100% {background-color:red; left:0px; top:0px;}
          }
        </style>
      </head>
    <body>
      <h1>CSS Animation</h1>
      <p>This example uses six of the animation properties:</p>
      <div></div>
    </body>
    </html>
    ```