## jQuery namespace ('jQuery' and '\$')

jQuery is the starting point for writing any jQuery code. It can be used as a function jQuery(...) or a variable jQuery.foo. \$ is an alias for jQuery and the two can usually be interchanged for each other (except where
`jQuery.noConflict()`; has been used - see Avoiding namespace collisions).

Assuming we have this snippet of HTML -

`<div id="demo_div" class="demo"></div>`

Now we might want to add some text on the div content using jQuery. To do that we can either use jQuery function or \$ -

`jQuery('#demo_div').text('Demo text');`

or

`$('#demo_div').text('Demo text');`

Both will result the same final HTML -

`<div id="demo_div" class="demo">Demo text</div>`

As `$` is more concise than jQuery it is generally the preferred method of writing jQuery.
