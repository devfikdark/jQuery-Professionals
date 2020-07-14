## Section 2.5: DOM Elements as selectors

```js
$(".elements").each(function(){
  //the current element is bound to `this` internally by jQuery when using each
  var currentElement = this;

  //at this point, currentElement (or this) has access to the Native API
  //construct a jQuery object with the currentElement(this)
  var $currentElement = $(this);
  
  //now $currentElement has access to the jQuery API
});
```