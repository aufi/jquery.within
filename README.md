jquery.within
=============

***just a concept, not working yet***

A jquery plugin which should make easier working with elements having same selectors, which are repeated in the page.

Bit dirty, but could be helpful.

Example
-------

```html
<form action="" id="edit_item_1">
<input name="item[name]" id="item_name">
<input name="item[amount]" id="item_amount">
<span class="price"></span>
</form>
<form action="" id="edit_item_2">
<input name="item[name]" id="item_name">
<input name="item[amount]" id="item_amount">
<span class="price"></span>
</form>
```

```javascript
$.within('form', function(~){
  ~('#item_amount').change(function(ev) {
    ~('span.price').html(10 * ev.target.val());
  });
});
```