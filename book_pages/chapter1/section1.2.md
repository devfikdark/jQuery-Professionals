## Avoiding namespace collisions

Libraries other than jQuery may also use \$ as an alias. This can cause interference between those libraries and libraries. To release \$ for use with other libraries:

`jQuery.noConflict();`

After calling this function, \$ is no longer an alias for jQuery . However, you can still use the variable jQuery itself to access jQuery functions:

`jQuery('#hello').text('Hello, World!');`

**Optionally**, you can assign a different variable as an alias for jQuery:

```js
// assigning jQuery.noConflict() to a variable **jqy**
var jqy = jQuery.noConflict();

// calling **jqy** for reference
jqy("#hello").text("Hello, World!");
```

Another simple way to secure jQuery's \$ alias and make sure DOM is ready:

```js
jQuery(function ($) {
  // DOM is ready and you can use **$** alias
  $("#hello").text("Hello, World!");
});
```
