# The-World-of-CSS-Selectors


> Universal Selector: - it selects everything in the document
>


```
* {
    background-color: cyan;
}
```

&nbsp;

> Element Selector: - this selects everything of a given type
>

**Pl:**
```
button {
    font-size: 30px;
}
```

**Pl:**
```
img {
    width: 100px;
    height: 200px;
}
```

&nbsp;

> Selector list:  - select all h1's and h2's elements
>

```
h1,h2 {
    color: darkmagenta;
}
```

&nbsp;

> The ID Selector - just for one
>

You add an ID to the markup and then you reference it using the name of the ID and the # sign.

**.html**

```
<button id="signup">Sign Up</button>
```

**.css**

```
#signup {
    background-color: #1d3557;
    color: #f1faee;
}
```

&nbsp;

> The Class Selector - for multiple
>
You add an ID to the markups and then you reference it using the name of the ID and the . sign.

**.html**

```
<span class="tag">dogs</span>
<span class="tag">funny</span>
```

**.css**


```
.tag {
    background-color: #e63946;
    color: #f1faee;
    font-size: 12px;
}
```

&nbsp;

> Descendant Selector
>

Select all ```<a>```'s that are nested inside an ```<li>```

**.html**
```
<section>
    <ul>
        <li><a href="">Home</a></li>
        <li><a href="">About</a></li>
    </ul>
</section>
```
**.css**
```
li a {
    color: teal;
}
```

OR can combinate with the **Class Selector**



**.html**
```
<section class="post">
    <h2>This Corgi got some good stuff from the vet.<span class="tag">dogs</span></h2>
    <button>+Vote</button>
</section>
```

**.css**
```
.post h2{
    color:#457b9d;
}
```

&nbsp;

> Adjacent Selector: +
>

- Select only the buttons that are immediately preceded by an ```<h2>```
```
h2 + button{
    font-size: 20px;
}
```

&nbsp;

> Direct Child Selector >
>

- Select only the anchor tag that are direkt children of the footer element
```
footer > a {
    color: #a8dadc
}
```

&nbsp;

> Attribute Selector
>

- Select all input elements where the type attribute is set to "password"

**.html**
```
<input type="text" placeholder="Search">
<input type="password" placeholder="password">  <!-- just here changed the color>
```

**.css**

```
input[type="password"]{
    color: red;
}
```

&nbsp;

> Pseido Classes
>

```:hover```

- hover over a button inside of a post (class="post")
```
.post button:hover
{
    background-color: #e63946;
    color: #f1faee;
}
```

```:active```

- active,when click on a button
```
.post button:active{
    background-color: #02c39a;
}
```

```:checked```

- when,its checked (radiobutton,checkbox) than change the color etc..



```:nth-of-type```

- when, i wanted to make every 2. or every 5. then using this

**Pl:**
```
.post:nth-of-type(3n) {
    background-color: #dfe8dc ;
}
```

&nbsp;

> Pseudo Elements: ::
>

Keyword added to a selector that lets you style a particular part of selected element(s)

```::after```

```::before```

```::first-letter```

```::first-line```

```::selection```

**Pl.:**

Make the first line of the paragraph puprle
```
p::first-line{
    color: purple;
}
```

**Pl.:**

Make the background color yellow , when its selected
```
p::selection{
    background-color: yellow;
}
```

**Pl.:**

Make the first letter of the h2 bigger
```
h2::first-letter{
    font-size: 45px;
}
```

&nbsp;

> Specificity
>

Specificity is how the browser decides which rules to apply when multiple rules could apply to the same element.

It is a measure of how specific a given selector is. The more specific selector "wins".



>> ID > CLASS > ELEMENT

**Pl.:** 

**1 element selector [0>0>1]**
```
p{
    color: yellow;
}
```
vs

**2 element selector [0>0>2] - WIN**
```
section p {
    color: puprle;
}
```

**PL.:**

**1 ID Selector - WIN**
```
#submit {
    color: olvie;
}
```
vs

**1 Class 2 Element Selector**
```
nav a .active {
    color: orange;
}
```

&nbsp;

> Specificity
> Inline Styles - ```style=" "```

it is more specific than IDs and classes and elements - Inline Styles > ID > Classes > Elements

**.html**
```
<button id="signup" style="color: red">Sign Up</button>
```

&nbsp;

> Specificity
> Important declaration - !important

it'll just ignore specifity and just make something win automatically

**.css**
```
button {
    background-color: magenta !important;
}
```
