## Loading jQuery via console on a page that does not have it

Sometimes one has to work with pages that are not using jQuery while most developers are used to have jQuery
handy.
In such situations one can use Chrome Developer Tools console ( <kbd>F12</kbd> or <kbd> Ctrl + Shift + i </kbd> ) to manually add jQuery on a loaded page
by running following.

```js
var j = document.createElement("script");
j.onload = function () {
  jQuery.noConflict();
};
j.src = "https://ajax.googleapis.com/ajax/libs/jquery/1.12.4/jquery.min.js";
document.getElementsByTagName("head")[0].appendChild(j);
```
