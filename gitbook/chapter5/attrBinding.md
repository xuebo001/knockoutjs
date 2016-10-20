attr 绑定提供了一种方式可以设置DOM元素的任何属性值。你可以设置img的src属性，连接的href属性。使用绑定，当模型属性改变的时候，它会自动更新。

```
<a data-bind="attr: { href: url, title: details }">
    Report
</a>
<script type="text/javascript">
var viewModel = {
        url: ko.observable("year-end.html"),
        details: ko.observable("Report including final year-end statistics")
    };
</script>
```
呈现结果是该连接的href属性被设置为year-end.html， title属性被设置为Report including final year-end statistics

