## Section 2.1: Overview

### Basic selectors

```js
$("*") // all elements
$("div") // all <div> elements
$(".blue") // all elements with class=blue
$(".blue.red") // all elements with class=blue AND class=red
$(".blue,.red") // all elements with class=blue OR class=red
$("#headline") // all (first) element with id=headline
$("[href]") // all elements with an href attribute
$("[href='example.com']") // all elements with href=example.com
```

### Relational operators

```js
$("div span") // all <span>s that are descendants of a <div>
$("div > span") // all <span>s that are a direct child of a <div>
$("a ~ span") // all <span>s that are siblings following an <a>
$("a + span") // all <span>s that are immediately after an <a>
```