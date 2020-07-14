## Section 2.6: HTML strings as selectors

```js
function template(href,text){
  return $("<div><a href='" + href + "'>" + text + "</a></div>");
}
```

```html
<div>
  <a href="google.com">Google</a>
</div>
```

If called as: 
```js 
template("google.com","Google").
```
