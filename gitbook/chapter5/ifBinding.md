使用if binding可以控制某个组件动态显示，类似我们之前接触到的visible属性

```html
<script type="text/javascript" src="knockout-2.2.0.js">
</script>
<label>
    <input type="checkbox" data-bind="checked: displayMessage" />
    Display message
</label>
<div data-bind="if: displayMessage">
    Here is a message. Astonishing.
</div>
<script type="text/javascript">
    ko.applyBindings({
        displayMessage: ko.observable(false)
    });
</script>

```
此例根据checkbox是否勾选来控制是否显示下面的一个`<div>`



