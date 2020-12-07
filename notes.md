```js
$('#add-logical').unbind('click').click(function(){
  // $("#logical").clone().appendTo($(".sortable")).selectmenu({width: 125});
  $("<li data-item='test' id='test'><span class='draggable'></span><span class='remove'></span></li>").appendTo($(".sortable"));
  var menu = getLogicalMenu();
  $(menu).clone().appendTo($("#test .draggable")).selectmenu({width: 125});
  $(".sortable").sortable("refresh");
});

function getLogicalMenu() {
  return `<select name="logical" id="logical" class="ui-selectmenu-menu ui-widget ui-corner-all">
    <option value="AND">AND</option>
    <option value="OR">OR</option>
  </select>`;
}
```