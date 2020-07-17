## Section 5.2: jQuery 2.2.3 and earlier

These are all equivalent, the code inside the blocks will run when the document is 
ready:

```js
$(function() {
  // code
});

$().ready(function() {
  // code
});

$(document).ready(function() {
  // code
});

jQuery(function() {
  // code
});
```