## The jQuery Object

Every time jQuery is called, by using `$()` or `jQuery()`, internally it is creating a new instance of jQuery. This is the [source code](http://code.jquery.com/jquery-2.2.4.js) which shows the new instance -

```js
// Define a local copy of jQuery
jQuery = function (selector, context) {
  // The jQuery object is actually just the init constructor 'enhanced'
  // Need init if jQuery is called (just allow error to be thrown if not included)
  return new jQuery.fn.init(selector, context);
};
```

Internally jQuery refers to its prototype as .fn , and the style used here of internally instantiating a jQuery object
allows for that prototype to be exposed without the explicit use of new by the caller.

In addition to setting up an instance (which is how the jQuery API, such as .each , children , filter , etc. is exposed),
internally jQuery will also create an array-like structure to match the result of the selector (provided that something
other than nothing, undefined , null , or similar was passed as the argument). In the case of a single item, this array-
like structure will hold only that item.

A simple demonstration would be to find an element with an id, and then access the jQuery object to return the
underlying DOM element (this will also work when multiple elements are matched or present).

```js
var $div = $("#myDiv"); //populate the jQuery object with the result of the id selector
var div = $div[0]; //access array-like structure of jQuery object to get the DOM Element
```
