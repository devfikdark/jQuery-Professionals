## Section 4.1: Differece between attr() and prop()

**attr()** gets/sets the HTML attribute using the DOM functions `getAttribute()` and `setAttribute()`. 

**prop()** works by setting the DOM property without changing the attribute. In many cases the two are interchangeable, but occasionally one is needed over the other.

To set a **checkbox as checked** :
```js
$('#tosAccept').prop('checked', true); // using attr() won't work properly somethime here
```

To **remove a property** you can use the `removeProp()` method. 

To **remove attributes** you can use the `removeAttr()` method. 
