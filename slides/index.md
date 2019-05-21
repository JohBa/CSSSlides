- title : Quick Intro: CSS
- description : A quick introduction into CSS
- author : Johannes Baeurle, Jan Reinhardt
- theme : league
- transition : default

***

## Quick Intro: CSS

<img style="border-style: none" border="0" src="images/AIT-Logo_small.jpg" />

### **Johannes Baeurle & Jan Reinhardt**, AIT GmbH <br /> [@JoBaeurle](http://twitter.com/JoBaeurle) | [github JohBa](https://github.com/JohBa) | [aitgmbh.de](http://www.aitgmbh.de/)

***

### Roadmap

 - **CSS**
 - SASS
 - B/Fulma

---

### CSS

**C**ascading **S**tyle **S**heets

CSS describes how HTML elements are to be displayed on screen, paper, or in other media.

---

### Add CSS

#### Inline

```html
<p style="color:blue;">This is a Blue Paragraph</p>
```

<p style="color:blue;">This is a Blue Paragraph</p>

---

### Add CSS

#### Internal

```html
<style>
h1   {color: blue;}
p    {color: red;}
</style>
```

<h1 class="sample1">This is a heading</h1>
<p class="sample1">This is a paragraph.</p>

---

### Add CSS

#### External

```html
<head>
  <link rel="stylesheet" href="styles.css">
</head>
```

---

### Syntax

```css
Selector1 [, Selector2 [, …] ] {
    Key-1: Value-1;
    …
    Key-n: Value-n[;]
}
```

https://www.w3schools.com/cssref/

---

### Selectors

<img src="images/selectors.png" style="background: white;" width=500 />
<a href="https://www.w3schools.com/cssref/css_selectors.asp">https://www.w3schools.com/cssref/css_selectors.asp</a>

---

### IDs

- Each element can have only one ID
- Each page can have only one element with that ID
- Anchor on webpage (e.g. http://url.com#firstname)

```css
#firstname {
  color: yellow;
}
```

```html
<span id="firstname">Firstname</span>
```

<span id="firstname">Firstname</span>

' spezielle browserfunktionalität, anker auf webseite
' bei Eingabe URL scrollt automatisch zu Element mit ID

---

### Classes

- You can use the same class on multiple elements.
- You can use multiple classes on the same element.
- Classes and Ids

```css
.widget { background-color: purple; }
.widget2 { border: 1px dashed white !important; }
```

```html
<div class="widget">Widget</div>
<div class="widget widget2">Widget</div>
<div class="widget" id="firstname">Widget with id</div>
```

<div class="widget">Widget</div>
<div class="widget widget2">Widget</div>
<div class="widget" id="firstname">Widget with id</div>

' Analogie barcode und seriennummer
' barcode für produktfamilie, gibt preis und art produkt an
' seriennummer für einzelnes objekt zur identifikation

---

### element element

```css
div .inside {
  background-color: green;
}
```

```html
<div>
  <div class="inside">Inside</div>
</div>
```

<div>
  <div class="inside">Inside</div>
</div>

' Selects all "inside" elements inside "div" elements
' tiefe egal, daher hier schlecht zeigbar

---

### element > element

```css
.parent { border: 1px solid white }
.parent > .child { background-color: green; }
```

```html
<div class="parent">
  <div class="inner">Inside</div>
  <span class="child">Child</span>
</div>
<div><span class="child">Child</span></div>
```

<div class="parent">
  <div class="inner">Inside</div>
  <span class="child">Child</span>
</div>
<div><span class="child">Child</span></div>

' Selects all "child" elements where the parent is a "parent" element

---

### :hover

```css
.hoversample:hover { background-color: green; }
```

```html
<div>
  <span class="hoversample">Child</span>
</div>
```

<div>
  <span class="hoversample">Child</span>
</div>

---

### ::after ::before

```css
.aftersample::after { content: "after"; }
.beforesample::before { content: "before"; }
```

```html
<div>
  <p class="aftersample">Container</p>
  <p class="beforesample">Container</p>
</div>
```

<div>
  <p class="aftersample">Container</p>
  <p class="beforesample">Container</p>
</div>

---

### :nth-child()

```css
.altlist li:nth-child(2n) { background-color: gray; }
```

```html
<ul class="altlist">
  <li>item</li>
  <li>item</li>
  <li>item</li>
  <li>item</li>
</ul>
```

<ul class="altlist">
  <li>item</li>
  <li>item</li>
  <li>item</li>
  <li>item</li>
</ul>

---

### transition

```css
.transition {
  width: 100px;height: 100px; background: red;
  transition: width 2s; -webkit-transition: width 2s;
}
.transition:hover { width: 300px; }
```

```html
<div class="transition"></div>
```

<div class="transition"></div>

' Browsersupport beachten!

---

### Display

```css
.inline { display: inline; }
.block { display: block; }
.inline-block { display: inline-block; }
```

<div style="border:1px dashed white !important">
Lorem ipsum dolor sit amet <p class="inline">INLINE!</p> Vestibulum volutpat tellus diam, consequat gravida libero rhoncus ut.
</div>
<div style="border:1px dashed white !important">
Lorem ipsum dolor sit amet<p class="block">BLOCK!</p> Vestibulum volutpat tellus diam, consequat gravida libero rhoncus ut.
</div>
<div style="border:1px dashed white !important">
Lorem ipsum dolor sit amet <p class="inline-block">INLINE-BLOCK!</p> Vestibulum volutpat tellus diam, consequat gravida libero rhoncus ut.
</div>

---

### Flexbox

```css
.flexcontainer { display: flex; flex-direction: row; flex-wrap: wrap; }
.flexblock { background: green; border: 1px solid white; }
```

```html
<div class="flexcontainer">
  <div class="flexblock"></div>
  <div class="flexblock"></div>
  <div class="flexblock"></div>
  <div class="flexblock"></div>
</div>
```

<div class="flexcontainer">
  <div class="flexblock"></div>
  <div class="flexblock"></div>
  <div class="flexblock"></div>
  <div class="flexblock"></div>
</div>

Einführung unter https://css-tricks.com/snippets/css/a-guide-to-flexbox/

Demo!

' Demo zeigen...

---

### Browser support

<img src="images/browsersupport.png" style="background: white;" width=550 />
<a href="https://www.w3schools.com/cssref/css3_browsersupport.asp">https://www.w3schools.com/cssref/css3_browsersupport.asp</a>
<a href="https://caniuse.com">https://caniuse.com</a>

---

### Limitations

- own functions?
- variables?
- inheritance?

<img src="images/varsupport.png" style="background: white;" width=550 />

' css ist limitiert
' sass/scss (preprocessor) als lösung

---

***

### Roadmap

 - CSS
 - **SASS**
 - B/Fulma

---

### Syntactically Awesome StyleSheets

(or SCSS -> other syntax)

- preprocessor
- variables
- nesting
- mixins
- own functions
- extend/inheritance

---

### Variables

```css
$font-stack:    Helvetica, sans-serif
$primary-color: #333

body
  font: 100% $font-stack
  color: $primary-color
```

---

### Nesting

```css
nav
  ul
    margin: 0
    padding: 0
    list-style: none

  li
    display: inline-block
```

```css
nav ul {
  margin: 0;
  padding: 0;
  list-style: none;
}

nav li {
  display: inline-block;
}
```

---

### Mixins

```css
=transform($property)
  -webkit-transform: $property
  -ms-transform:     $property
  transform:         $property

.box
  +transform(rotate(30deg))
```

```css
.box {
  -webkit-transform: rotate(30deg);
  -ms-transform: rotate(30deg);
  transform: rotate(30deg);
}
```

---

### Own functions

```css
$random = 2

@function column-width($col, $total:8) {  
 @return percentage($col/($total+$random));  
}

.col-3
 width: column-width(3, 8);  

```

```css
.col-3 {  
 width: 30%;  
}
```

---

### Extend/inheritance

```css
%message-shared
  border: 1px solid #ccc
  color: #333

.message
  @extend %message-shared

.success
  @extend %message-shared
  border-color: green
```

```css
.message, .success {
  border: 1px solid #cccccc;
  color: #333;
}

.success {
  border-color: green;
}
```

---

### SCSS

- other (verbose) syntax

```css
=transform($property)
  -webkit-transform: $property
  -ms-transform:     $property
  transform:         $property

.box
  +transform(rotate(30deg))
```

```css
@mixin transform($property) {
  -webkit-transform: $property;
      -ms-transform: $property;
          transform: $property;
}

.box { @include transform(rotate(30deg)); }
```

' klammern, semikolon, teils einfache symbole statt wörter

---

***

### Thank you!

* Too many sources, see Sources.txt
* Jan, Johannes
