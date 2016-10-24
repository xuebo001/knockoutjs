html绑定到DOM元素上，使得该元素显示的HTML值为你绑定的参数。如果在你的view model里声明HTML标记并且render的话，那非常有用。

```html
<div data-bind="html: details"></div> 
<script type="text/javascript">
var viewModel = {        
details: ko.observable() // Initially blank    
};    
viewModel.details("<em>For further details, 
view the report <a href='report.html'>here</a>.</em>"); // HTML content appears
</script>

```


