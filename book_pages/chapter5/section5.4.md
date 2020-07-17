## Section 5.4: Attaching events and manipulating the DOM inside ready()

Example uses of `$(document).ready()`

- **Attaching event handlers**

```js
$(document).ready(function() {
  $("button").click(function() {
    // Code for the click function
  });
});
```


- **Run jQuery code after the page structure is created**

```js
jQuery(function($) {
  // set the value of an element.
  $("#myElement").val("Hello");
});
```

- **Manipulate the loaded DOM structure**

For example: hide a div when the page loads for the first time and show it on the 
click event of a button

```js
$(document).ready(function() {
  $("#toggleDiv").hide();
  $("button").click(function() {
    $("#toggleDiv").show();
  });
});
```