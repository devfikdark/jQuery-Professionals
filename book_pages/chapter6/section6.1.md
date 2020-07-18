## Section 6.1: Delegated Events

```html
<html>
  <head>
  </head>
  <body>
    <ul>
      <li>
        <a href="/route-1">Link 1</a>
      </li>
      <li>
        <a href="/route-2">Link 2</a>
      </li>
      <li>
        <a href="/route-3">Link 3</a>
      </li>
    </ul>
  </body>
</html>
```

```js
$('ul').on('mouseover', 'a', function () {
  console.log(this.href); // show route URL
});
```