## Section 6.2: Attach and Detach Event Handlers


### Attach an Event Handler

- **HTML**
```html
<button id="foo">bar</button>
```

- **jQuery**
```js
$( "#foo" ).on( "click", function() {
  console.log( $( this ).text() ); //bar
});
```

### Detach an Event Handler

- **HTML**
```html
<button id="hello">hello</button>
```

- **jQuery**
```js
$('#hello').on('click', function(){
  console.log('hello world!');
  $(this).off();
});
```

When clicking the button $(this) will refer to the current jQuery object and will remove all attached 
event handlers from it.

- **jQuery**
```js
$('#hello').on('click', function(){
  console.log('hello world!');
  $(this).off('click');
});

$('#hello').on('mouseenter', function(){
  console.log('you are about to click');
});
```

In this case the **mouseenter** event will still function after clicking.