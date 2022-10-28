<h1>HTML</h1>
HTML stands for Hyper Text Markup Language. It is a language used to make websites. A HTML file is made of 2 things.<br>
1) Elements <br>
2) Their Attributes

<h1> HTML Anatomy </h1>
The very basic structure of a HTML document consists of a html,head, body elements. The (!DOCTYPE html) is added at the start of every document. It is a document type declaration which is a set of guidelines and regulations that must be attached to a certain online document(html,xml etc).

```sh
<!DOCTYPE html>
<html lang="en" dir="ltr">
  <head>
    <meta charset="utf-8">
    <title></title>
  </head>
  <body>
    
  </body>
</html>
```
<h1>Elements</h1>
There are many types of HTML elements. Some of them are 
<h2> HTML HEADINGS</h2>

```sh
<h1> Heading 1 </h1>
<h2> Heading 2 </h2>
<h3> Heading 3 </h3>
<h4> Heading 4 </h4>
<h5> Heading 5 </h5>
<h6> Heading 6 </h6>
```
which looks like this:<br>
<img src="https://user-images.githubusercontent.com/95839946/197925075-dae3c4be-80fe-4e9d-a767-a63b0dcf7a17.png" width="240">

<h2>PARAGRAPH TAG</h2>
It is one of the basic tags of HTML. It is used to define certain text as paragraph.

```sh
<p>This is a part of a paragraph </p>
```

OUTPUT:
This is a part of a paragraph.<br>
<br>
<ul>
<li>To italisize text in html we can use the italic or emphasise tags.Italic tag italisises the text inside it ,that is, it styles the text to make it slanted. But the text inside the em or emphasise tag is stresses and emphasised.
  
```sh
This is <i> italic </i>
This is <em> emphasised </em>
```
This is *italic* <br>
This is * emphasised*
  <li> To make text bold 2 tags can be used. Bold or strong.
     
```sh
This is <b> bold </b>
This is <strong> strong </strong>
``` 
OUTPUT:<br>
    This is __bold__ <br>
    This is **strong**
    
  </ul>
  They can be together used in paragraph tag as follows.
       
```sh
  <p> I am <em> writing </em> a <strong>HTML</strong> cheatsheet.    
``` 
which looks like this:<br>
    I am *writing* a **HTML** cheatsheet.<br>
    
<h2>HTML LISTS </h2>
There are 2 types of lists in HTML. 
<h4>
---> Ordered list(ol) <br>

</h4>
An ordered list is something that renders a list which is numbered. The various items inside a list are specified using (li) tag.
  
```sh
<ol>
 <li>This</li>
 <li>is</li>
 <li>an</li>
 <li>ordered list</li>
</ol>
```
OUTPUT:<br>
<ol>
 <li>This</li>
 <li>is</li>
 <li>an</li>
 <li>ordered list</li>
</ol>
  <br><br>
<strong>Attributes</strong><br>
1. Type:
  Sets the numbering type
  
  ```sh
<ol type="a">
 <li>a for lowercase letters
</ol>
<ol type="A">
 <li>A for uppercase letters
</ol>
<ol type="i">
 <li>i for lowercase Roman numerals
</ol>
<ol type="I">
 <li>I for uppercase Roman numerals
</ol>
<ol type="I">
 <li>1 for numbers (default)
</ol>
```  
OUTPUT:<br>
<img src="https://user-images.githubusercontent.com/95839946/197957813-eabfb331-0c41-43ae-b59e-81ea493ef0ff.png" width="280">   

2. Start: Used to change the starting numbering value. For example, to start a ordered list from 6 we can specify start ="6".
   
```sh
<ol start ="6" type="a">
<li>This</li>
<li>is</li>
<li>an</li>
<li>ordered list</li>
</ol>
```   
OUTPUT:<br>
<ol start ="6" type="a">
<li>This</li>
<li>is</li>
<li>an</li>
<li>ordered list</li> 
   </ol>
  <br>
---> Unordered list(ul) <br>
   An unordered list is something that renders a list which is bulleted. The various items inside a list are specified using (li) tag.
     
```sh
<ul>
 <li>This</li>
 <li>is</li>
 <li>an</li>
 <li>unordered list</li>
</ul>
```
OUTPUT:<br>
<ul>
 <li>This</li>
 <li>is</li>
 <li>an</li>
 <li>unordered list</li>
</ul>
 <br>
<strong>Attributes</strong><br><br>
   1. Type:
  Sets the type of bullets
  
  ```sh
 <ul type="circle">
  <li>circle
 </ul>
 <ul type="disc">
  <li>disc
 </ul>
 <ul type="square">
  <li>square
 </ul>
  ```   
  OUTPUT:<br>
  <ul type="circle">
  <li>circle
 </ul>
 <ul type="disc">
  <li>disc
 </ul>
 <ul type="square">
  <li>square
 </ul>
 <h2>HTML IMAGE ELEMENTS </h2>
 Images can be added to HTML using the (img) tag. But the image tag is not enough, we should also specify the source(src attribute) of the image to display a particular image.The source can be either local or on the web.
 
  ```sh
<img src="image.png">
  ```   
The various attributes of image are:
<ul>
 <li>src- Specifies the path to the image</li>
 <li>alt-Specifies an alternate text for the image, if the image for some reason cannot be displayed</li>
 <li>width- Specifies the width of the image</li>
 <li>height- Specifies the height of the image</li>
</ul>
 <h2>HTML LINKS ANCHOR TAGS</h2> 
 The HTML <a> tag also known as the HTML anchor tag is used to specify a hyperlink to link one page to another. The hyperlink can be created to another web page or a file, a location, or a URL. To link to destination page or URL, the “href” attribute is used with the HTML anchor tag.
  
   ```sh
<p> This is linked to 
  <a href="https://github.com"> Github </a>
</p>
  ``` 
  OUTPUT:<br>
  <p> This is linked to 
  <a href="https://github.com"> Github </a>
  </p><br>
To apply the styles styled using CSS in the file styles.css we can use links.
  
   ```sh
<link rel="stylesheet" href="styles.css">
  ```   
 <h2>HTML TABLES</h2>   
  A HTML table contains rows and columns.To declare a table we use the (table) tag. To add rows to the table (tr)- table row tag can be used. To specify table hedings (th) tag can be used.To add data inside a table cell (td) tag is used. Columns can be created using both (th) and (td) tags. The contents inside (th) tag are bold.
  
   ```sh
<table>
  <tr>
    <th>Column-1</td>
    <th>Column-2</td>
    <th>Column-3</td>
  </tr>
  <tr>
    <td>Text-1</td>
    <td>Text-2</td>
    <td>Text-3</td>
  </tr>
  <tr>
    <td>Content-1</td>
    <td>Content-2</td>
    <td>Coontent-3</td>
  </tr>
</table>
   ```   
  OUTPUT:<br>
<table>
  <tr>
    <th>Column-1</td>
    <th>Column-2</td>
    <th>Column-3</td>
  </tr>
  <tr>
    <td>Text-1</td>
    <td>Text-2</td>
    <td>Text-3</td>
  </tr>
  <tr>
    <td>Content-1</td>
    <td>Content-2</td>
    <td>Coontent-3</td>
  </tr>
</table>  

 <h2>HTML FORMS</h2>   
 An HTML form is used to collect user input. The user input is most often sent to a server for processing.The HTML (form) element is used to create an HTML form for user input.The (form) element is a container for different types of input elements, such as: text fields, checkboxes, radio buttons, submit buttons, etc.The HTML (input) element is the most used form element.

An (input) element can be displayed in many ways, depending on the type attribute.

Here are some examples:
<table>
<tr>
<th>Type</th>
<th> Description</th>
</tr>
<tr>
<td>Text</td>
<td>Displays a single-line text input field</td>
</tr>
<tr>
<td>Radio</td>
<td>Displays a radio button (for selecting one of many choices)</td>
</tr>
<tr>
<td>Checkbox</td>
<td>Displays a checkbox </td>
</tr>
<tr>
<td>Submit</td>
<td>Displays a submit button  </td>
</tr>
<tr>
<td>Button</td>
<td>Displays a clickablebutton  </td>
</tr>
</table>

The (label) tag defines a label for many form elements.The for attribute of the (label) tag should be equal to the id attribute of the <input> element to bind them together.

```sh
<label for="name">Your Name:</label>
<input type="text" id="name"><br>
<label for="yes">Yes </label>
<input type="Radio" id="yes"><br>
<label for="no">No</label>
<input type="checkbox" id="no"><br>
<input type="submit">
 ```   
 OUTPUT:<br>
<img src="https://user-images.githubusercontent.com/95839946/197953388-8c580552-16e5-4e3c-96da-2d706600e120.png" width="275">
<br>
<br>
For further information regarding HTML elements and their attributes,refer to:<br>
<a href = "https://www.w3schools.com/html">https://www.w3schools.com/html</a><br>
<a href = "https://developer.mozilla.org/en-US/docs/Web/HTML">https://developer.mozilla.org/en-US/docs/Web/HTML</a><br>
<hr>
