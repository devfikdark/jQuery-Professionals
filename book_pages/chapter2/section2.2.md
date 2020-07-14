## Section 2.2: Types of Selectors

In jQuery you can select elements in a page using many various properties of the 
element, including:

- Type
- Class
- ID
- Possession of Attribute
- Attribute Value
- Indexed Selector
- Pseudo-state

Take the following **HTML** for example:
```html
<a href="index.html"></a> <!--1-->
<a id="second-link"></a> <!--2-->
<a class="example"></a> <!--3-->
<a class="example" href="about.html"></a> <!--4-->
<span class="example"></span> <!--5-->
```

### Selecting by Type:

The following jQuery selector will select all `<a>` elements, including 1, 2, 3 and 4.
```js
$("a")
```

### Selecting by Class

The following jQuery selector will select all elements of class example (including 
non-a elements), which are 3, 4 and 5.
```js
$(".example")
```

### Selecting by ID

The following jQuery selector will select the element with the given ID, which is 2.
```js
$("#second-link")
```

### Selecting by Possession of Attribute

The following jQuery selector will select all elements with a defined href attribute, 
including 1 and 4.
```js
$("[href]")
```

### Selecting by Attribute Value

The following jQuery selector will select all elements where the href attribute exists 
with a value of `index.html`, which is just 1.
```js
$("[href='index.html']")
```

### Selecting by Indexed Position (Indexed Selector)

The following jQuery selector will select only 1, the second `<a>` ie. the second-link 
because index supplied is `1 like eq(1)` (Note that the index starts at 0 hence the 
second got selected here!).
```js
$("a:eq(1)")
```

### Selecting with Indexed Exclusion

To exclude an element by using its index `:not(:eq())`. The following selects `<a>` 
elements, except that with the class example , which is 1
```js
$("a").not(":eq(0)")
```

### Selecting with Exclusion

To exclude an element from a selection, use `:not()` The following selects `<a>` 
elements, except those with the class example , which are 1 and 2.
```js
$("a:not(.example)")
```

### Selecting by Pseudo-state

You can also select in jQuery using pseudo-states, including `:first-child`, 
`:last-child`, `:first-of-type` , `:last-of-type` , etc. The following jQuery selector 
will only select the first `<a>` element: number 1.
```js
$("a:first-of-type")
```

### Combining jQuery selectors
```js
$("a.class1.class2.class3#someID[attr1][attr2='something'][attr3='something']:first-of-type:first-child")
```

This would select an `<a>` element that:
- Has the following classes: class1, class2, and class3
- Has the following ID: someID
- Has the following Attribute: attr1
- Has the following Attributes and values: attr2 with value something , attr3 with value something
- Has the following states: first-child and first-of-type

```js
$("a, .class1, #someID")
```

This would select:
- All `<a>` elements
- All elements that have the class class1
- An element with the id #someID

### Child and Sibling selection

- To select a non-direct child, use a **space**
- To select a direct child, use **a >**
- To select an adjacent sibling following the first, use **a +**
- To select a non-adjacent sibling following the first, use **a ~**

### Wildcard selection

Select all elements inside #wrapper element
```js
$('#wrapper *')
```
