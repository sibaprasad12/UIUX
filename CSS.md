# CSS Tutorial (https://www.tutorialrepublic.com/css-tutorial/)
- It stands for Cascading Style Sheet
- It is used to style the HTML page
- Before CSS, style is added to all the html page and it become very huge and also difficult to maintain.
  
## What can you do with CSS
- easily apply same style rules on multiple elements.
- control the presentation of multiple pages of a website with a single style sheet.
- present the same page differently on different devices.
- style dynamic states of elements such as hover, focus, etc. that isn't possible otherwise.
- change the position of an element on a web page without changing the markup.
- alter the display of existing HTML elements.
- transform elements like scale, rotate, skew, etc. in 2D or 3D space.
- create animations and transitions effects without using any JavaScript.
- create print friendly version of your web pages.
  
## Advantages of Using CSS
- CSS Save Lots of Time
- Easy Maintenance
- Pages Load Faster
- Superior Styles to HTML
- Multiple Device Compatibility

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
## Understanding CSS Syntax
- h1 {color:blue; text-align:center;}
- here h1 -> selector  
       color -> Property  
       blue  -> Value  
       text-align  -> Another Property
       center  -> Value
- All properties are separated by semicolon
- You can add any number of properties
  
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
    
- **Element Type Selector**  This will applied to all the elements present in the html page
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
  
- **Descendant Selectors**  You can use these selectors when you need to select an element that is the descendant of another element,
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
## Common properties
- Color can be defined in these types hexadecimal, rgb or color name
- ```
      h1 {
        color: red; or color: #ff5722; or color: rgb(255, 165, 0);
      }
  ```
- **Background**
  - Background Color   -> h1 { background-color: #f0e68c; }
  - background-image   -> h1 {  background-image: url("images/tile.png");  }
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
  - ul {  list-style-type: square;  }
  - ol {  list-style-type: upper-roman; }
  - ol.in li { list-style-position: inside; }
-**Table**
  - table, th, td {  border: 1px solid black;  }
  - table {border-collapse: collapse;}
  - th, td { border: 1px solid black; }
  - table { width: 300px; table-layout: fixed or auto; }
## Some of the Advanced css tags   
- **outline** - 
- **cursor** - YOu can customize cursor when cursor move over the element
- **overflow** - When overflow text, it will show scroll
- **Units** - Only one character is bigger size as compared to other characters in that word
- **display** - span { display: block; } a {  display: block; } span { display: inline; } a {  display: inline-block; } a {  display: none; }
- **visibility** visible, hidden, collapse, inherit, 
- **position**
- **layering**
- 
