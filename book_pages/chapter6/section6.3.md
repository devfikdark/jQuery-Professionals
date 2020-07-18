## Section 6.3: Switching specific events on and o via jQuery. (Named Listeners)

Sometimes you want to **switch off** all previously registered listeners.

```js
/**** Example - 1 *****/
//Adding a normal click handler
$(document).on("click",function(){
  console.log("Document Clicked 1")
});

//Adding another click handler
$(document).on("click",function(){
  console.log("Document Clicked 2")
});

//Removing all registered handlers.
$(document).off("click")


/**** Example - 2 *****/
//Add named event listener.
$(document).on("click.mymodule",function(){
  console.log("Document Clicked 1")
});

$(document).on("click.mymodule",function(){
  console.log("Document Clicked 2")
});

//Remove named event listener.
$(document).off("click.mymodule");
```