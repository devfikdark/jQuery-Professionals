## Include script tag in head of HTML page

To load **jQuery** from official CDN (Content Delivery Network), go to the jQuery official [website](https://jquery.com/) or you can get the CDN from [cdnjs.com](https://cdnjs.com/libraries/jquery). There you'll find different versions of **jQuery** from where you can choose whatever version you need. But it is recommended to use the latest minified version. Copy the required link from the websites and put them in your head tag or before close body tag using `<script>` tag i.e -

`<script src="https://cdnjs.cloudflare.com/ajax/libs/jquery/3.5.1/jquery.min.js" integrity="sha512-bLT0Qm9VnAYZDflyKcBaQ2gg0hSYNQrJ8RilYldYQ1FxQYoCLtUjuuRuZo+fjqhx/qtq/1itJ0C2ejDxltZVFg==" crossorigin="anonymous"></script>`

**Example**:

```html
<!DOCTYPE html>
<html>
  <head>
    <title>Loading jquery-2.2.4</title>
    <script src="https://code.jquery.com/jquery-2.2.4.min.js" async></script>
  </head>
  <body>
    <p>This page is loaded with jquery.</p>
  </body>
</html>
```
