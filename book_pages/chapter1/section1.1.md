## Getting Started

Create a file hello.html with the following content:

```html
<!DOCTYPE html>
<html>
  <head>
    <title>Hello, World!</title>
  </head>
  <body>
    <div>
      <p id="hello">Some random text</p>
    </div>
    <script src="https://code.jquery.com/jquery-2.2.4.min.js"></script>
    <script>
      $(document).ready(function () {
        $("#hello").text("Hello, World!");
      });
    </script>
  </body>
</html>
```

Then run this code in your browser and you should see `Hello, World!` printed on your page.

## Setup jQuery

To get started with jQuery you need to load the jQuery library first from the jQuery CDN(Content Delivery Network):

`<script src="https://code.jquery.com/jquery-2.2.4.min.js"></script>`

After loading jQuery in your script tag or in .js file you need to define a function to be executed when the DOM(Document Object Model) is detected to be `ready` by jQuery:

```js
// When the `document` is `ready`, execute this function `...`
$(document).ready(function() { ... });

// A commonly used shorthand version (behaves the same as the above)
$(function() { ... });

```

Once the DOM is ready, jQuery executes the callback function shown above. Inside of our function, there is only one call which does 2 main things -

- Gets the element with the attribute equal to hello (our selector #hello). Using a selector as a passed argument is the core of jQuery's functionality and naming; the entire library essentially evolved from extending `document.querySelector`
- Set the `text()` inside the selected element to Hello, World!.

  \$('#hello').text('Hello, World!');

Select id `hello` by passing the hello selector and set the text on the element.
