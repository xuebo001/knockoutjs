style绑定是添加或删除一个或多个DOM元素上的style值.

```
<div data-bind="style: { color: currentProfit() < 0 ? 'red' : 'black' }">   
Profit Information
</div>
<script type="text/javascript">
var viewModel = {
        currentProfit: ko.observable(150000)
 // Positive value, so initially black 
   };
    viewModel.currentProfit(-50); 
// Causes the DIV's contents to go red</script>

```
当currentProfit 小于0的时候div的style.color是红色，大于的话是黑色

