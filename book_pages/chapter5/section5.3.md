## Section 5.3: jQuery 3.0

- **Notation**

As of `jQuery 3.0`, only this form is recommended:

```js
jQuery(function($) {
  // Run when document is ready
  // $ (first argument) will be internal reference to jQuery
  // Never rely on $ being a reference to jQuery in the global namespace
});
```

- **Asynchronous**

```js
$(function() {
  console.log("inside Morol");
});

console.log("outside Morol");
```

- **Output**
  - outside Morol
  - inside Morol