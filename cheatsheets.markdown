---
layout: page
title: Cheatsheet
permalink: /Cheatsheet/
---

# CSS CHEATSHEET

<!-- ! CHEATSHEET LINKS

// GCS[epic=LINKS] CS SYNTAX CSS

// GLINK /Users/kaw/Dropbox (Personal)/DEV/Working/00CHEATSHEETS/0 Shortcuts.js
// GLINK /Users/kaw/Dropbox (Personal)/DEV/Working/00CHEATSHEETS/0commenting.js
// GLINK /Users/kaw/Dropbox (Personal)/DEV/Working/00CHEATSHEETS/0colors.js
// GLINK /Users/kaw/Dropbox (Personal)/DEV/Working/00CHEATSHEETS/0SyntaxJS.js
// GLINK /Users/kaw/Dropbox (Personal)/DEV/Working/00CHEATSHEETS/0SyntaxHTML.html
// GLINK /Users/kaw/Dropbox (Personal)/DEV/Working/00CHEATSHEETS/0SyntaxCSS.css

-->

editorTextFocus && !editorReadonly && editorLangId =~ /^markdown$|^rmd$|^qmd$/
**bold**
*italics*
~~strikethrough~~

## CSS

https://developer.mozilla.org/en-US/docs/Glossary/CSS
https://developer.mozilla.org/en-US/docs/Learn/CSS

https://developer.mozilla.org/en-US/docs/Web/CSS
https://www.w3schools.com/cssref/index.php

### CSS (Cascading Style Sheets)

  - CSS is a style sheet language
    - CSS is NOT a markup language either
    - <span style="color:red">CSS is NOT a programming language</span>    
    - CSS is what you use to Selectively style HTML elements
  - CSS is a visual style and presentation of content written in HTML code
  
  * <span style="color:red">CSS also be used with other markup languages like:</span>
    - <span style="color:red">SVG (markup)</span>
    - <span style="color:red">XML (markup)</span>
    

  - Consists of Properties that format the content
    - Font, Text, Spacing, Layout, etc

  * "Cascading" refers to the rules that govern how Selectors are prioritized to change a page's appearance
    - <span style="color:red">This is a very important feature, since a complex website can have thousands of CSS rules</span>
    

  - A CSS rule is a set of Properties associated with a Selector 


## 3 TYPES OF CSS  

<!--GCS-CSS[epic=CS_CSS] 3 Types of CSS-->

### Inline CSS
  - inside an Element in the html file

<!-- GEXAMPLE[epic=CS_CSS] Inline CSS -->

```HTML
<p style="color blue>Blah Blah Blah</p>
```

### Internal CSS

  - `<style> </style> `inside the <head> Element
  * <span style="color:red">Inline causes Code Entanglement (CSS and HTML become entangled)</span>
  * <span style="color:red">Should never be used & Not proper coding format</span>
  * <span style="color:red">Separations of Concerns</span>
  

<!-- GEXAMPLE[epic=CS_CSS] Internal CSS -->

```HTML
<head>
    <style>
    p {
      color: blue;
    }
    </style>
  </head>
```

### External CSS

  - Style inside external CSS file (style.css)

<!-- GEXAMPLE[epic=CS_CSS] External CSS style.css -->

```CSS
h1 {
  color: blue;
  text-align: center;
  font-size= 20px;
}
```
## LINKING EXTERNAL CSS FILE

### `<link>` Element

<!-- GCS-HTML[epic=CS_HTML] Linking CSS Files-->
<!-- GCS-HTML[epic=CS_HTML_ELM] <link>-->
<!-- GCS-CSS[epic=CS_CSS] Linking CSS Files-->
<!-- GCS-CSS[epic=CS_CSS] <link>-->

  https://developer.mozilla.org/en-US/docs/Web/HTML/Element/link

```HTML
<link href="someCSSFile.css" rel="someValue">
```

  `<link>` is a Void Element

Standard Link Attributes include:

href
  
  - `<link>` specifies the "URL of the linked resource"
  - URL can be absolute or relative

rel

  - names a relationship of the "Linked document" to the "current document"
  - the attribute must be a space-separated list of link type value

title

  - has special Semantics on the `<link>` element - When used on a `<link rel="stylesheet">` 
  - it defines a "default" or an "alternate" stylesheet

- as
  - audio
    `<audio>` elements
  - document
    `<iframe>` and `<frame>` elements
  - embed
    `<embed>` elements
  - fetch 
    fetch, XHR
    * <span style="color:red">Note: This value also requires <link> to contain the crossorigin attribute.</span>
  - font 
    - CSS @font-face
  - image
    `<img>` and `<picture>` elements with srcset or imageset attributes, SVG `<image>` elements, CSS
    *-<span style="color:red">image rules</span>
  - object 
    `<object>` elements
  - script 
    `<script>` elements, Worker 
  - importScripts
  - style 
    `<link rel=stylesheet>` elements, CSS @import
  - track 
    `<track>` elements
  - video 
    `<video>` elements
  - worker 
    Worker, SharedWorker
- crossorigin
  - anonymous
  - use-credentials
- fetchpriority
  - high
  - low
  - auto
- hreflang
- imagesizes
- imagesrcset
- integrity
- media
- prefetch Secure context 
- referrerpolicy
  - no-referrer
  - no-referrer-when-downgrade
  - origin
  - origin-when-cross-origin
  - unsafe-url
- sizes
- type
- blocking

- disabled (deprecated)

- Non Standard Link Attributes include:
  - methods (deprecated)
  - target (deprecated)
- Obsolete attributes include:
  - charset (deprecated)
  - rev (deprecated)

### `rel="" `Attribute

<!--GCS-CSS[epic=CS_CSS] rel=""-->

https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes/rel

```HTML
<link href="someCSSFile.css" rel"someValue">
```

- Defines the relationship between a linked resource and the current document

- Valid on following Elements: 
- `<link>`
  - `<a>`
  - `<area>`
  - `<form>`


- the supported Values depend on the Element on which the attribute is found

- Standard Values include:

    ? stylesheet
      https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes/rel#attr-stylesheet
      
        ? rel= "stylesheet"

    ? alternate 
      ? alternative stylesheet
        https://developer.mozilla.org/en-US/docs/Web/CSS/Alternative_style_sheets

        ? rel= "alternative stylesheet"

    -  author
    -  bookmark
    -  canonical
    -  dns-prefetch
    -  external
    -  help
    -  icon
    -  license
    -  manifest
    -  me
    -  modulepreload
    -  next
    -  nofollow
    -  noopener
    -  noreferrer
    -  opener
    -  pingback
    -  preconnect
    -  prefetch
    -  preload
    -  prerender
    -  prev
    -  search
    -  tag

  - Non-Standard Values include:

    - apple-touch-icon

<!-- GEXAMPLE[epic=CS_CSS] <link rel"someValue" -->

```HTML
<link href="someFile.css" rel"style">
```

## DECLARATION & CSS RULE

### DECLARATION

  <!--GCS-CSS[epic=CS_CSS] DECLARATION BLOCK-->

- Select & Style an Elements in CSS

  - Consist of:

    ? Selector 

      - is the name of Element that is selected for styling, minus the < >

      ^ someElement

    ? Declartion or Style [ color: blue; ]

      ? Property 

        ^ [ color ]

      ? Value 

        ^[ blue ]


```CSS
someSelector {
  someProperty: someValue;
  someProperty: someValue;
}
```

<!-- GEXAMPLE[epic=CS_CSS] Simple CSS Ex -->

```CSS
h1 {
  color: blue;
  text-align: center;
  font-size= 20px;
}
```

### CSS RULE

  <!--GCS-CSS[epic=CS_CSS] CSS RULE-->

<!--GCS-CSS[epic=CS_CSS] -->

- 
- 
- 
- 
- 
- 
- 


## CLASSES & DEPENDENT SELECTORS

### Decendent Selectors

  <!--GCS-CSS[epic=CS_CSS] DECENDENT SELECTORS-->
  <!--GCS-CSS[epic=CS_CSS_CLASS] ???-->

  - Inheritence
  - Styling Child Elements

  ? parentElement childElement {}
  ? grandparentElement parentElement childElement {}

   
<!-- GEXAMPLE[epic=CS_CSS] Parent-Child Descendents -->
  

```CSS
footer p {
  font-size: 16px;
}
```
<!-- GEXAMPLE[epic=CS_CSS] Grandparent-Child Descendents -->

```CSS
article header p {
  font-style: italic;
}
```

### Class

<!-- GCS-CSS[epic=CS_CSS_CLASS] -->
