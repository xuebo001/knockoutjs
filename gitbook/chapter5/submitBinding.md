submit绑定只能用在表单form元素上。

```html
<form data-bind="submit: doSomething">
    ... form contents go here ...
    <button type="submit">Submit</button>
    </div>
    <script type="text/javascript">
        var viewModel = {
            doSomething: function(formElement) { // ... now do something        }    }; 
    </script>

```
KO将把整个form表单元素作为参数传递到你的submit绑定函数里




