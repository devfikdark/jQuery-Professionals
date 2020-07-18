## Section 6.5: Events for repeating elements without using ID's

- **HTML**

```html
<div class="item-wrapper" data-item_id="346">
  <div class="item">
    <span class="person">Fred</span>
  </div>
  <div class="item-toolbar">
    <button class="delete">Delete</button>
  </div>
</div>

<div class="item-wrapper" data-item_id="393">
  <div clss="item">
    <span class="person">Wilma</span>
  </div>
  <div class="item-toolbar">
    <button class="delete">Delete</button>
  </div>
</div>
```

- **jQuery**

```js
$(function() {
  $('.delete').on('click', function() {
    // "this" is element event occurred on
    let $btn = $(this);

    // traverse to wrapper container
    let $itemWrap = $btn.closest('.item-wrapper');

    // look within wrapper to get person for this button instance
    let person = $itemWrap.find('.person').text();

    // remove element
    $itemWrap.remove();
  });
});
```