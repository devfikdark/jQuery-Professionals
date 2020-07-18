## Section 6.6: Document Loading Event `.load()`

If you want your script to wait until a certain resource was loaded, such as an 
image or a PDF you can use `.load()` , which is a shortcut for shortcut for `.on( "load", handler)`.


- **HTML**

```html
<img src="image.jpeg" alt="image" id="image">
```

- **jQuery**

```js
$( "#image" ).load(function() {
  // run script
});
```