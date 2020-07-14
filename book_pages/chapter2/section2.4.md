## Section 2.4: Combining selectors

```html
<ul class="parentUl">
  <li> Level 1
    <ul class="childUl">
      <li>Level 1-1 <span> Item - 1 </span></li>
      <li>Level 1-1 <span> Item - 2 </span></li>
    </ul>
  </li>
  <li> Level 2
    <ul class="childUl">
      <li>Level 2-1 <span> Item - 1 </span></li>
      <li>Level 2-1 <span> Item - 1 </span></li>
    </ul>
  </li>
</ul>
```

### Descendant and child selectors

Given a parent `<ul>` - parentUl find its descendants (`<li>`),
```js
- This gets all matching descendants of the specified ancestor all levels down.
  - $('parent child')
  - $('ul.parentUl li')

- This finds all matching children (only 1st level down).
  - $('parent > child')
  - $('ul.parentUl > li')

- This works same as 1. above.
  - $('child','parent')
  - $('li','ul.parentUl')

- This works same as 1. above.
  - find() - $('parent').find('child')
  - $('ul.parentUl').find('li')

- This works same as 2. above.
  - children() - $('parent').find('child')
  - $('ul.parentUl').children('li')
```

### Other combinators

- Group Selector : ","
  - Select all `<ul>` elements AND all `<li>` elements AND all `<span>` elements :
    - $('ul, li, span')

- Multiples selector : "" (no character)
  - Select all `<ul>` elements with class parentUl
    - $('ul.parentUl')

- Adjacent Sibling Selector : "+"
  - Select all `<li>` elements that are placed immediately after another `<li>` element:
    - $('li + li')
    
- General Sibling Selector : "~"
  - Select all `<li>` elements that are siblings of other `<li>` elements:
    - $('li ~ li')