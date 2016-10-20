css绑定是添加或删除一个或多个CSS class到DOM元素上。

```
<div data-bind="css: { profitWarning: currentProfit() < 0 }"> 
  Profit Information
</div> 
<script type="text/javascript">
var viewModel = {
        currentProfit: ko.observable(150000)
        // Positive value, so initially we don't apply the "profitWarning" class    
};    
viewModel.currentProfit(-50);    
// Causes the "profitWarning" class to be applied
</script>

```
当数字变成负数时高亮显示

