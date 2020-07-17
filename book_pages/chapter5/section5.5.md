## Section 5.5: Difference between $(document).ready() and $(window).load()

`$(document).ready()` waits until the **full DOM is availble** -- all the elements 
in the HTML have been parsed and are in the document. However, resources such as 
images may not have fully loaded at this point. If it is important to
wait until all resources are loaded, `$(window).load()` and you're aware of the 
significant limitations of this event then the below can be used instead:

```js
$(document).ready(function() {
  console.log($("#my_large_image").height()); // may be 0 because the image isn't available
});

$(window).load(function() {
  console.log($("#my_large_image").height()); // will be correct
});
```