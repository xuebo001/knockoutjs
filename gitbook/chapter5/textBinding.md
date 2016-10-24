Text绑定主要是让DOM元素显示参数值。如下例：

```html
Today's message is: <span data-bind="text: myMessage"></span>
<script type="text/javascript">   
 var viewModel = {      
  myMessage: ko.observable() // Initially blank  
  };    
viewModel.myMessage("Hello, world!"); // Text appears
</script>



```


