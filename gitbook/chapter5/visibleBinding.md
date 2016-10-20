Visible绑定通过绑定一个值来确定DOM元素显示或隐藏.如下例：

```
<div data-bind="visible: shouldShowMessage"> 
 You will see this message only when "shouldShowMessage" holds a true value.
</div>
<script type="text/javascript">
    var viewModel = { shouldShowMessage: ko.observable(true)    };
    viewModel.shouldShowMessage(false); // ... now it's hidden 
viewModel.shouldShowMessage(true); // ... now it's visible again
</script>


```


