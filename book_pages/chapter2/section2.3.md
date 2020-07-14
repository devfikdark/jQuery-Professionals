## Section 2.3: Caching Selectors

```js
let nav = $('#navigation');
nav.show();

// Or

$('#navigation').show();
```

```html
<div class="parent">
  <div class="child">Child 1</div>
  <div class="child">Child 2</div>
</div>

<script>
  let children = $('.child');
  let firstChildText = children[0].text();
  console.log(firstChildText);
  // output: "Child 1"
</script>
```

```html
<div class="parent"></div>

<script>
  let parent
  = $('.parent');
  let children = $('.child');
  console.log(children);
  // output: []
  parent.append('<div class="child">Child 1</div>');
  children = $('.child');
  console.log(children[0].text());
  // output: "Child 1"
</script>
```
