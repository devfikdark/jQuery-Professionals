## Section 4.2: Get the attribute value of a HTML element

When a single parameter is passed to the `.attr()` function it returns the value of passed attribute on the selected element.

**Syntax**:
```js
$([selector]).attr([attribute name]);
```

**Example**:
```js
- HTML:
<a href="/home">Home</a>

- jQuery:
$('a').attr('href');

Output: /home
```

### Fetching data attributes:

jQuery offers `.data()` function in order to deal with data attributes. .data function returns the value of the data attribute on the selected element.

**Syntax**:
```js
$([selector]).data([attribute name]);
```

**Example**:
```js
Html:
<article data-column="69"></article>

jQuery:
$("article").data("column");

Output: 69
```