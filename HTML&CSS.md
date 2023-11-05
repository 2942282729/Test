# HTML Fundamental

HTML Is a Markup language, which called Hyper Text Markup Language.

## HTML  structure

```HTML
<!DOCTYPE html>
<!-- Every HTML document always needs to start with this so-called DOCTYPE -->
<!-- The purpose is to let the browser know that we are actually using HTML in this file and all browsers will then
     know that they should use the HTML5 specifications to render this file 
-->
<html lang="en">
      <!-- the default borwser language is setted to English -->
  <head>
      <!-- the head element is basically for things that are not visible in browser window -->
    <meta charset="UTF-8" />
      <!--Set the browser's character to UTF-8.-->
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Document</title>
      <!-- External CSS -->
    <link rel="stylesheet" href="style.css" />
        <!-- Internal CSS -->
    <style>
      /* {} is the declaration block */
      /* seperate our HTML and CSS */
      /* h1 {
        color: blue;
      } */
    </style>
  </head>

  <body>
    </body>
</html>

```

## Semantic HTML

First of all,it is crucial for us to know semantic HTML. 

### The definition of semantic HTML:

 What I mean is that certain elements have actually a meaning or a purpose attach to them,so when we think about a certain HTML element, we should actually not think about what that element looks like as it's rendered on the page. But instead we should think about what that element actually means and what it stands for. 

### Why should we use sematic HTML?

1. Search engine optimization which basically means that a search engine such as Google will be able to understand the structure of your content. And therefore they will be better able to analyse what your content and what your web page is all about.

2. Writing semantic HTML is extremely important for accessibility and especially for people who rely on screen readers to consume on web pages.

3. I also want to make it very clear from the very beginning that when we think about HTML, we should not only think about how it

   actually looks like in  the browser, but even more about what these elements actually mean and what they stand for.

## HTML Element

### body

The body element is the parent of all the other elements in our HTML document

```html

<body>
    
</body>
```



### style	

Setting the style of html elements

```html
 <style>
     h1 {
      color: blue;
    } 
  </style>
```



### link

```html
<link rel="stylesheet" href="style.css">			//import CSS file
```



style and link are placed inside head.



### a（anchor ）

```html
<a>
     href="https://developer.mozilla.org/zh-CN/"      <-- inside href is the url of the page ->
     target="_blank"> 						<--target is a property of how the page was opened ->
     MDN Web Docs.
</a>
```



### em

<em> means emphasize  

```html
<em>fundamental</em>
```

![image-20231105102234295](C:\Users\haoChen\AppData\Roaming\Typora\typora-user-images\image-20231105102234295.png)

italic 

```html
<i>fundamental</i>
```

![image-20231105102328532](C:\Users\haoChen\AppData\Roaming\Typora\typora-user-images\image-20231105102328532.png)

In HTML 5, we use em element instead of the i element.



### strong



```html
 <P>
        <!-- strong elements can be displayed in bold but it do not have semantics -->
        Posted by <strong>Laura Jones </strong>on Monday, June 21st 2027
</P>
```



### ul (unordered list )



```html
 <!-- undered-list -->
	<ul>
        <!-- sematics:list item -->
        <li>To be able to use the fundamental web dev language</li>
        <li>To hand-craft beautiful websites instead of relying on tools like Worpress or Wix</li>
        <li>To build web applications</li>
        <li>To impress friends</li>
        <li>To have fun 😃</li>
    </ul>
```



### ol (ordered list )

```html
 <!-- ordered-list -->
    <ol>
        <!-- sematics:list item -->
        <li>The opening tag</li>
        <li>The closing tag</li>
        <li>The actual element</li>
    </ol>
```



### p (paragraph)

```html
<P>

        In this post, let's focus on HTML.

        We will learn what HTML is all about,

        and why you too should learn it.

</P>
```



### img (image)

```html
 <img 
      src="laura-jones.jpg"                          //resource Address of the photo
      alt="Headshot of laura-jones" 
      //Photo captions, care for the visually impaired, access to browser resources using screen readers
      width="50px" 								//Photo display width
      height="50px"							   //Photo display height
 >
```





### h1~h6 (title)

```html
<h1>Level 1 title</h1>
```



### New in HTML5

#### header

```HTML
<header> 
	Writing the header content of a web page
</header>
```

#### nav

```html
<nav>
		Write the contents of the navigation bar
</nav>
```



#### article

```html
<article>
Write the content of the article, here the article refers to the broad scope, not only text, but also can be put into other elements, such as video, images, etc.
<article/>
```



#### aside

Secondary information on the page

```html
<aside>
	Posts related to arcticle content  
</aside>
```



#### footere

```html
<footer>
    Copyright &copy;2027 by the Code Magazine             
    <!--The copyright information at the end &copy are html entities, you can check the table to find some useful entities-->
</footer>

```

Here is the link of [HTML entities.](https://css-tricks.com/snippets/html/glyphs/), which is the web page written by my teacher [Jonas Schmedtmann](https://twitter.com/jonasschmedtman)

# CSS Fundamental

## 2.1 Definition of  CSS

CSS means Cascading Style Sheets it is also one of the core technologies of the web

## 2.2 Application

We use CSS to describe the visual style and presentation of the content that we previous wrote using HTML. CSS consists of countless properties that developers use to format the content properties about font , text, general spacing,layout of the page,etc. 

Each properties can take different types of values, such as length or key words. 

## 2.3 Constitute

<img src="C:\Users\haoChen\AppData\Roaming\Typora\typora-user-images\image-20231029190730349.png" alt="image-20231029190730349" style="zoom:50%;" />



## 2.4 Setting style 

#### Inline CSS

Inline CSS is not recommended to use. It is written inside of each element.

```HTML
  <h1 style="color:blue">📘 The Code Magazine</h1>
```



 <h1 style="color:RGB(40,135,245)">📘 The Code Magazine</h1>



#### Internal CSS

Internal CSS is written inside of the header of the html file.

```CSS
 <style>
  h1 {
      color: blue;
    } 
  </style>
```





#### external CSS

external CSS is a CSS file which CSS styles are written in it.

```HTML
<link rel="stylesheet" href="style.css">			//import external CSS file
```



## 2.5 Selector

### 2.5.1 Types:

#### Important  Key  Word

Usually, we don't use this selector unless it's absolutely necessary.

```HTML
<footer>
    <p id="Copyright">
      Copyright &copy; 2027 by The Code Magazine.
    </p>
  </footer>
```



```CSS
footer p {
    font-size: 16px;
      /* important selector owns the highest priority  */
    color: green !important;
}

```

#### Universal selector

The Universal selector is useful if we actually want a certain property applied to all elements but which does not get inherited. So the universal selector simply applies to all the elements, and there is no inheritance involved. And therefore, this is perfect if you want to apply a certain property, that does not automatically get inherited to all the elements. On the other hand, any elements we put into the body gets inherited. And so that's completely different mechanism than using the universal selector.

```html
* {
  /* border-top:7px solid green;  */
  /* This kind of global reset is actually extremely common  */
  margin: 0;
  padding: 0;
  /* it actually can be easily overwritten */
}

```



#### Element Selector

```CSS
h1 {
    color: blue;
    font-size: 26px;
    /* Set text to uppercase */
    text-transform: uppercase;
    /* Set the form of the font to italic */
    font-style: italic;
}


```



#### List  Selector

```CSS
h1,
h2,
h3,
h4,
p,
li {
    /* sans-serif(typography) */
    font-family: sans-serif;
}
```



#### Descendant selector

```CSS
footer p {
    font-size: 16px;
}
```



#### Hash Selector(ID Selector)

```CSS
 <p id="Copyright">
      Copyright &copy; 2027 by The Code Magazine.
    </p>
```

ID can not be repeatly used.



#### Class Selector

```CSS
.main-header {
    background-color: #f7f7f7;
}
```



#### Pseudo Selector

 We can actually have CSS automatically figure out which is the first li element inside of a container.

```html
<ul>
          <!-- the li element is the first element of its parent ul element -->
          <!-- so if we use pseudo class to style the fist li elemnt in ul, the li element must be the first 			element of the ul element
        in this case,p element is the first element of the ul,so the pseudo class dosen't work -->
          <!-- let's comment it -->
          <!-- <p>test</p> -->
          <!-- And then the pseudo class will work, and the first li will be styled to bold -->
          <li class="first-li">
            To be able to use the fundamental web dev language
          </li>
          <li>
            To hand-craft beautiful websites instead of relying on tools like
            Worpress or Wix
          </li>
          <li>To build web applications</li>
          <li>To impress friends</li>
          <li>To have fun 😃</li>
        </ul>
```



```CSS
/* use a pseudo class */

/* Style the first child of its parent elements */

li:first-child {
    /* the first li element will be bolded */
    font-weight: bold;
}

li:last-child {
    /* the last li element will be italic */
    font-style: italic;
}

li:nth-child(2) {
   /*the color of the second li element will be red.*/
    color: red;
}

/* set all the odd element to be red */
li:ntn:nth-child(odd)
{
  color:red
}

/* we can also do even */
 li:nth-child(even) {
  color: blue;
}

/* This techneque is quite useful, for example, to style tables, which oftentimes have like alterning background colors */
```

The pseudo-class selector selects the elements in the current list in the order in which they are selected.

#### link Style

Now we will learn how style hyperlinks using pseudo classes

```CSS
/* Styling Links
   We shouldn't simply select the anchor and style it instead we should style a pseudo class of the anchor
   because that will then allow us to target different states */
/* Remenber thar when we set pseudo class for the anchor element, the order is LVHA! */
/* The first one is the link pseudo class */

/* a:link only target at anchor elments that do actually have href(Hypertext Reference) attribute  */
a:link {
  color: #170fff;
  /* get rid of the underline */
  text-decoration: none;
}

/* the visited pseudo class */
a:visited {
  /* set the anchor's color after visiting the anchor */
  color: #170fff;
}

/* the hover pseudo class */
/* In the hover pseudo class we can define any styles that we want to be applied to the anchor
   as soon as the element is hovered by the mouse
*/
a:hover {
  color: orange;
  /* set the decoration of the link while it is horvered by the mouse */
  text-decoration: underline dotted orange;
}

/* active pseudo class */
/* This is the state in which we are actually clicking */
/* So when we do actually click on a link, then the act of pseudo class is edited to the element and we can then select
   that here like this.
*/
a:active {
  background-color: black;
  font-style: italic;
}

/* 
  These four states are always defined in this exact order, always link,visited,hover and active  (LVHA) 
*/

/* A couple of fundamental and really important theoretical concepts that we really need to undstand to master CSS */
```



#### Universal Selector

The Universal selector is useful if we actually want a certain property applied to all elements but which does not get inherited. So the universal selector simply applies to all the elements, and there is no inheritance involved. And therefore, this is perfect if you want to apply a certain property, that does not automatically get inherited to all the elements. On the other hand, any elements we put into the body gets inherited. And so that's completely different mechanism than using the universal selector.

```CSS
* {
  /* border-top:7px solid green;  */
  /* This kind of global reset is actually extremely common  */
  margin: 0;
  padding: 0;
  /* it actually can be easily overwritten */
}
```



### 2.5.2  Conflicts between Selectors:

The priority of different selectors

1. The highest priority is the declarations marked with the important keyword.(!)
2. The next is Inline styles
3. The next is the ID selector(#ID-name{}), and if there are multiple ID selectors, then it is the last of those selectors that get apply
4. The next in the priority is the Class selector or a Pseudo class selector. （.class-name{}）And, again, if there are multiple ones of those, then it is the last selector of those in the code that get applied. 
5. Then the next is the Element selector(div p a li...)
6. And then is the Universal Selector（*）which is the one with the lowest priority of all.

To sum it up: Important key word(!) > Inline Style > ID Selector > Class Selector or Pseudo Selector >Element Selector > Universal Selector(*)

When a selector is faced with conflicting attributes, it will decide on the conflicting attribute values based on the selector's priority, and for the rest of the non-conflicting parts, the rules set within the selector will still work.

### 2.5.3  Resolving style conflicts

What we should probably do is to write simpler selectors. Always write our selectors as simple as possible, and do not add too much

 nesting, or don't add too many IDs, and classes all in the same selector.

##  2.6 Element Display property

### Block element

Element like body, main, header, footer, section, nav, aside, div, h1-h6, p, ul, ol, li, etc.

Block element will occupy the entire width of the parent element, each block element will occupy a whole line. 

Here is the example

<img src="C:\Users\haoChen\AppData\Roaming\Typora\typora-user-images\image-20231105092151386.png" alt="image-20231105092151386" style="zoom: 50%;" />

### Inline element

Like the strong element, e m element and the anchor element.

The inline element actually occupy exactly the space that is needed for its contents. They also don't create any line breaks after or before the element. And so therefore they can simply stay inside of their parent elements without creating any additional space.

Here is the example. 

![image-20231105092810791](C:\Users\haoChen\AppData\Roaming\Typora\typora-user-images\image-20231105092810791.png)

Keep in mind, for inline elements, the height and width property do not have any effect. Also paddings and margins are only applied horizontally or in other words, on the left and right sides, but not on the top and bottom.   





### Inline-block element

Change the inline element to block element, we can do that with the display property set to the value of block.