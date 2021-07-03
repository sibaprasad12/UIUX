# CSS Tutorial (https://www.tutorialrepublic.com/css-tutorial/)

- It stands for Cascading Style Sheet
- It is used to style the HTML page
- HTML is just a layut of webpage and we add style to webpage using CSS.
- Before CSS, style is added to all the html page and it become very huge and also difficult to maintain.

## What can you do with CSS

- Easily apply same style rules on multiple elements.
- Control the presentation of multiple pages of a website with a single style sheet.
- Present the same page differently on different devices.
- Style dynamic states of elements such as hover, focus, etc. that isn't possible otherwise.
- Change the position of an element on a web page without changing the markup.
- Alter the display of existing HTML elements.
- Transform elements like scale, rotate, skew, etc. in 2D or 3D space.
- Create animations and transitions effects without using any JavaScript.
- Create print friendly version of your web pages.

## Advantages of Using CSS

- CSS Save lots of time
- Easy Maintenance
- Pages Load Faster
- Superior Styles to HTML
- Multiple Device Compatibility

## What is DOM ?

- DOM stands for document Object Model.
- When a page is loaded, the browser creates a DOM of the page which is constructed as a Tree of objects

## HTML id and class attribute

- WHen an HTML element is given an id, it serves as an unitue identifier for that element
- On the Other hand, when an HTML element is given a class, it now belongs to that class.
- More than one element can belongs to a single class but every element must have a unique ID(if assigned)
- We can add multiple classes to an element like this

```
<div id = "first" class = c1 c2 c3>>
...
</div>
```

- Here first is the unique id
- Multiple classes followed by spaces.
- In above code, c1, c2, c3 is given to the same element <div>

## How to include CSS in html page

- There are 3 ways to do this

1. Inline styles — Using the style attribute in the HTML start tag
2. Embedded styles — Using the <style> element in the head section of a document
3. External style sheets — Using the <link> element, pointing to an external CSS file

## Inline Styles

```
    <h1 style="color:red; font-size:30px;">This is a heading</h1>
    <p style="color:green; font-size:22px;">This is a paragraph.</p>
    <div style="color:blue; font-size:14px;">This is some text content.</div>
```

## Embedded styles

```
    <html lang="en">
    <head>
        <title>My HTML Document</title>
        <style>
            body { background-color: YellowGreen; }
            p { color: #fff; }
        </style>
    </head>
    <body>
        <h1>This is a heading</h1>
        <p>This is a paragraph of text.</p>
    </body>
    </html>
```

## External style sheets

- Create another style.css file and include in the html page like this
- Include the style.css file inside head tag
- In below Example style.css is the file where all styles declared

```
  <head>
      <title>My HTML Document</title>
      <link rel="stylesheet" href="css/style.css">
  </head>
```

## How to import external Style sheet

- ```
        <style>
        @import url("css/style.css");
        p {
            color: blue;
            font-size: 16px;
        }
      </style>

      @import url("css/layout.css");
      @import url("css/color.css");
      body {
        color: blue;
        font-size: 14px;
      }
  ```

## Another way to import extrrnal Style sheet

- Create a CSS style file named **style.css** in the same folder with all the defined style
- Define the style.css in style sheet like below

```
  <!DOCTYPE html>
  <html lang="en">
  <head>
      <meta charset="UTF-8">
      <meta http-equiv="X-UA-Compatible" content="IE=edge">
      <meta name="viewport" content="width=device-width, initial-scale=1.0">
      <title>Document</title>
  <!-- Define your css here -->
  <link rel="stylesheet" href="style.css">
  </head>

  <body>
  </body>
  </html>
```

## Understanding CSS Syntax

- ```
      h1 {
          color:blue;
          text-align:center;
          }
  ```
- here h1 -> selector  
   color -> Property  
   blue -> Value  
   text-align -> Another Property  
   center -> Value
- All properties are separated by semicolon
- You can add any number of properties

## What is CSS Selector

- A CSS selector is used to select an HTML elemtnt(s) for styling

```
body{
  color: red;
  background: pink;
}
```

- After each property inside style, there must be a semicolon
- In above code color, background are the property name and the values are defined after a colon

## Selector

- Selector means combinely you can assign style to many element in a single html web page.
- There are different selectors
- **Universal Selector** THis means you can apply the style to all the elements in the html page
- ```
      * {
          margin: 0;
          padding: 0;
      }
  ```
- This will remove all the padding and margin from all the elements given in any html elements like <p> <div> <h1> etc.

- **Element Type Selector** This will applied to all the elements present in the html page
- ```
    p {
        color: blue;
    }
  ```
- This will change all the color of the paragraph present in the html page
- **ID selector** will apply to all the ids given to the element name, for example
- ```
      #error {
          color: red;
      }
  ```
- Color of all the element change to red
- **Class Selectors** will apply to all the class name defined in the style
- ```
    .blue {
        color: blue;
    }
  ```
- ```
      p.blue {
          color: blue;
      }
  ```
- The style rule inside the selector p.blue renders the text in blue of only those <p> elements that has class attribute set to blue, and has no effect on other paragraphs.
- **Descendant Selectors** You can use these selectors when you need to select an element that is the descendant of another element,
- ```
      ul.menu li a {
          text-decoration: none;
      }
  ```
- The style rules inside the selector ul.menu li a applied to only those <a> elements that contained inside an <ul> element having the class .menu, and has no effect on other links inside the document.
- **Child Selector** is used to select only those elements that are the direct children of some element.
- ```
      ul > li {
          list-style: square;
      }
      ul > li ol {
          list-style: none;
      }
  ```
- **Adjacent Sibling Selectors** The adjacent sibling selectors can be used to select sibling elements (i.e. elements at the same level). This selector has the syntax like: E1 + E2, where E2 is the target of the selector.
- ```
    h1 + p {
        color: blue;
        font-size: 18px;
    }
    ul.task + p {
        color: #f0f;
        text-indent: 30px;
    }
  ```
- In the above example if p is the immediate element after h1 in the html tag tree, the the first style is applied to that p element
- In the second case, if ul class name is task and the p is the immediate element after this id, then the style will be applied to the p element

- **General Sibling Selector** is same as the Adjecent sibling selector, but it will apply to all the adjecent element.
- ```
      h1 ∼ p {
          color: blue;
          font-size: 18px;
      }
      ul.task ∼ p {
          color: #f0f;
          text-indent: 30px;
      }
  ```
- In the above example, the first style will be apply to all the <p> which are after the <h1> element in the tree.
- The second style will apply to all the <p> element which is after <ul class="task"> in the html tree.

- **Grouping Selector** if a particular style is apply to some of the elements, instead of declaring style individually we can define once like this
- ```
        h1,h2,h3  {
            common properties
        }
  ```
  > > You can define multiple class names in one element separated by space

# 1.Common properties

- Color can be defined in these types hexadecimal, rgb or color name
- ```
      h1 {
        color: red; or color: #ff5722; or color: rgb(255, 165, 0);
      }
  ```
- **Background**
  - Background Color -> h1 { background-color: #f0e68c; }
  - background-image -> h1 { background-image: url("images/tile.png"); }
  - background-repeat
  - background-attachment
  - background-position
- **Font**
  - font-family
  - font-style
  - font-weight
  - font-size
  - font-variant
- **Text**
  - text-color
  - text-align
  - text-decoration
  - text-transform
  - text-indent
  - line-height
  - letter-spacing
  - word-spacing
- **link**
  - a:link — define styles for normal or unvisited links.
  - a:visited — define styles for links that the user has already visited.
  - a:hover — define styles for a link when the user place the mouse pointer over it.
  - a:active — define styles for links when they are being clicked.
- **List**
  - ul { list-style-type: square; }
  - ol { list-style-type: upper-roman; }
  - ol.in li { list-style-position: inside; } -**Table**
  - table, th, td { border: 1px solid black; }
  - table {border-collapse: collapse;}
  - th, td { border: 1px solid black; }
  - table { width: 300px; table-layout: fixed or auto; }

## Some of the Advanced css tags

- **outline** -
- **cursor** - YOu can customize cursor when cursor move over the element
- **overflow** - When overflow text, it will show scroll
- **Units** - Only one character is bigger size as compared to other characters in that word
- **display** - span { display: block; } a { display: block; } span { display: inline; } a { display: inline-block; } a { display: none; }
- **visibility** visible, hidden, collapse, inherit,
- **position**
- **layering**

# 2.Colors and Background

- CSS rules are simple key-value pairs with a selector we can write CSS rules o change color and set backgrounds

## The color property

- CSS color property can be used to set the text color inside an element

```
p {
  color :  red // text color will be changed to red with element name p
}
```

- Similarly we can set color for different elements.

## TYpes of color values

- FOllowing are the most commonly used color values in CSS
- **RGB** Specify color using RED, GREEN, BLUE values, eg rgb(200, 98,70)
- **HEX CODE** specify color using hash code values of colors, eg #d3d3d3
- **HSL** Specify the color using hsl values, eg hsl(8%, 90%, 63%)
- HSL - Hue Saturation Lightness
  > > THe value of the color or background color is provided as any one of these values
  > > We also have an RGBA and HSLA values for color but they are rarely used by beginners. A stands for alpha

## The Background-color property

- THe CSS background-color property specifies the background color of a container
- for example

```
.brown{
  background-color : brown;
}
```

## Background-image property

- Used to set an image as the background

```
body{
    background-image: Url("image.png")
}
```

- THe image is by default repeated in X and Y directions

## THe background-repeat property

- can be any one of these
- **repeat-x** -> Repeat in horizontal direction
- **repeat-y** -> Repeat in vertical direction
- **no-repeat** -> Image not Repeat
  > > See more posible values at MDN docs

## THe background-size property

- Can be following
- **cover** -> Fits and no empty space remains
- **contain** -> Fits and Image is fully visible
- **auto** -> Display in original size
- **{{width}}** -> Set width & height will be set automatically
- **{{width}} {{height}}** -> Set width & height
  > > Always check the MDN docs to check a given CSS property. Remember practice will make you perfect

## Background-position property

- Set the starting position of a background image

```
div{
    background-position : left top;
}
```

## background-attachment property

- Defines a scrollable Or non-scrollable character of a background image

```
div2{
  background-attachment : fixed
}
```

## Background shorthand property

- A single property to set multiple background properties

```
div3{
    background: red URL('img.png') no-repeat fixed right top;
}
```

- One of the properties acan be missing given the others are in order

# 3.Box Model

- The CSS Box model looks at all the HTML elements as boxes
- One Box another, like h1 is one box inside another box body
- With properties like padding, boarder margin

## Setting width and height

- We can set width and height in CSS as follows

```
  #box {
    height : 70px;
    width : 70 Px;
  }
```

> > The total Width/Height is calculated as follows
> > total height = height + top|bottom padding + top|bottom boarder + top|bottom margin

## Setting margin and padding

- We can set margin and padding as follows

```
.box{
  margin : 3px;   // sets top, bottom,left and right values for both the parameters
  padding : 3px;
}
```

## another way

```
boxMargin {
  margin : 7px 0px 2px 11px  (top, right bottom left) clockwise
}

boxLast {
    margin: 7px 3px (top & bottom left & right)
}
```

- We can also set individual margins/paddings like this

```
boxMargin {
  margin-top : 9px;
  margin-bottom : 8px;
  margin-left : 7px;
  margin-right : 6px;
}
```

## Setting boarders

- We can set the boarders as follows

```
.bx{
  boarder-width : 2px;
  boarer-style : solid;
  boarder-color : red;
}

or

.bx{
  boarder : 2px solid red;
}
```

## Boarder Radious

- We can set boarder radioud to create rounded boarders

```
div2{
    boarder-radious : 7px;

}
```

## Margin Collapse

- When 2 margins from different elements overlap, the equevelent margin is the greater of the two. THis is known as margin collpse

## Box sizing

- Determine what out of padding and boarder is included in elements width and height can be content-boox or boarder-box

```
div1{
    box-sizing : boarder-box;
}
```

- The content width and height incudes content + padding + boarder

# 4.Font and Display

## display property

- The CSS display property is used to determine whether an element is treated as a block/ inline elemtn and the layout used for its children(flexbox/grid/ etc)

## display-inline

- Taakes only the space required by the element.
- No linemarks before and after setting width/height not allowed.

## display : block

- Takes full space available in width and leaves a new line before and after the element

## display inline-block

- Similar to inline but setting height, width, margin and padding is allowed.
- Elements can sit next to each other

## display none vs visibility : hidden

- With display: none, the element is removed from document flow. It's space is not blocked
- with visibility: hidden, the element is hidden but it's space is reserved

## text align property

- Used to set the norizontal alignment of a text

```
div{
    text-align : center;
}
```

## text decoration property

- Used to decorate the text
- Can be overline, line through, underline, none

## text transfer property

- Used to specify uppercase and lowercase letters in a text

```
p.uppercase{
  text-transfer : uppercase;
}
```

## Line height property

- Used to specify the space between lines

```
.small{
  line-height : 0.7;
}
```

## font

- Font plays a very important role in the look and feel of a website

## font-family

- Font family specifies the font of a text
- CAn hold multiple values as a fallback system

```
p{
  font-family : "times new roman", monospace;
}
```

> > Always do this to ensure the correct font of your choice is rendered

## Web safe fonts

- These fonts are universally installed across browser

## How to add Google fonts

- IN order to use custom google fonts, go to google fonts
- Then select a style and finally paste it to the style.css of yout page

## Other font properties

- Some of the other font properties are listed below
- font-size
- font-style
- fontvariant

## Generic families

- Broad class of similar font eg serif, sans-serif
- Just like when we say fruit, it can be any fruit

## font-family -> specific

## generic-family -> Generic

# 5.Size position and List

- There are more units for describing size other than px.
- There are rem, cm, vw, vh, percentage etc

## Whats wrong with pixels ?

- Pixels(px) are relative to the viewing device.
- For a device with size 1920x1080, 1 px is 1 unit out of 1080/1920

### Relative lengths

- These units are relative to the other length property
- Following are some of the most commonly used relatives length

### em

- Unit relative to the parent font size.
- Em means My parent elements font size

### rem -> unit relative to the root font size {html tag}

### VW -> Unit relative to 1% Viewport width

### vh -> Unit relative to 1% of viewport height

### % -> Unit relative to the parent element

## min/max-height/width property

- CSS has a min-height, max-height, min-width, max-width property
- If the content is smaller than the minimum height minimum height will be applied.
- Similar is the case with other related properties.

## Position property

- Used to manipulate the location of an element
- FOllowing are the possible values
- **static** the default position - top|bottom|left|right|Z-index has no effect
- **relative** The top|bottom|left|right|Z-index will now work otherwise the element is in the flow of the document like static
- **fixed** Just like absolute except the element is positioned relative to the browser window.
- **Sticky** The elements is positioned based on user's scroll position

# List style properties

- The list style property is a shorthand for type, position and image

```
ul {
  list-style : square inside url('heavy.jpg')
}
```

- square -> list style type
- inside -> list style position
- url -> list style image

### Z-index prperty

- The Z-index property specifies the stack order of an element
- It defines which layer will be above which in case of overlapping elements.

# 6.Flexbox

# 7.CSS grid and Media Query

-

# 8. Transform Transition and Animation
