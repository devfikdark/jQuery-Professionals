## Section 3.1: jQuery each function

**HTML**:
```html
<ul>
  <li>NodeJs</li>
  <li>jQuery</li>
  <li>MongoDb</li>
</ul>
```
**Script**:
```js
$( "li" ).each(function( index ) {
  console.log( index + ": " + $( this ).text() );
});
```
A message is thus logged for each item in the list:
- 0: NodeJs
- 1: jQuery
- 2: MongoDb