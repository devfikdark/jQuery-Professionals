## Section 5.1: What is document-ready and how should I use it?

`jQuery` code is often wrapped in jQuery(function($) { ... }); so that it only runs 
after the DOM has finished loading.

```html
<script type="text/javascript">
  jQuery(function($) {
  // this will set the div's text to "Hello".
    $("#myDiv").text("Hello");
  });
</script>

<div id="myDiv">Text</div>
```

This is important because jQuery (and JavaScript generally) cannot select a `DOM` 
element that has not been rendered to the page.

```html
<script type="text/javascript">
  // no element with id="myDiv" exists at this point, so $("#myDiv") is an
  // empty selection, and this will have no effect
  $("#myDiv").text("Hello");
</script>

<div id="myDiv">Text</div>
```