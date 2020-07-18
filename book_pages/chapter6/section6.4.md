## Section 6.4: originalEvent

Sometimes there will be properties that aren't available in jQuery event. To access 
the underlying properties use `Event.originalEvent` Get Scroll Direction.

```js
$(document).on("wheel",function(e){
  console.log(e.originalEvent.deltaY)
  /*
    Returns a value between -100 and 100 depending on the direction you 
    are scrolling
  */
})
```