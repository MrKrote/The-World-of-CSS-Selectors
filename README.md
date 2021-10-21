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

> Direct Child Selector >
>

- Select only the anchor tag that are direkt children of the footer element
```
footer > a {
    color: #a8dadc
}
```
