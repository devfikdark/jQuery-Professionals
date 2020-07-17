## Section 5.6: Difference between jQuery(fn) and executing your code before `</body>`

Using the document-ready event can have small performance drawbacks, with 
**delayed** execution of up to **~300ms**. Sometimes the same behavior can be 
achieved by execution of code just before the closing `</body>` tag:

```html
<body>
  <span id="greeting"></span> world!
  <script>
    $("#greeting").text("Hello");
  </script>
</body>
```

will produce similar behavior but perform sooner than as it does not wait for the 
document ready event trigger as it does in:

```html
<head>
  <script>
    jQuery(function($) {
      $("#greeting").text("Hello");
    });
  </script>
</head>
<body>
  <span id="greeting"></span> world!
</body>
```

Emphasis on the fact that **first example** relies upon your knowledge of your page 
and placement of the script just prior to the closing `</body>` tag and specifically 
after the span tag.