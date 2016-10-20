click绑定大部分是用在button，input和连接a上，但是可以在任意元素上使用。

```
<div>
    You've clicked
    <span data-bind="text: numberOfClicks">
    </span>
    times
    <button data-bind="click: incrementClickCounter">
        Click me
    </button>
</div>
<script type="text/javascript">
    var viewModel = {
        numberOfClicks: ko.observable(0),
        incrementClickCounter: function() {
            var previousCount = this.numberOfClicks();
            this.numberOfClicks(previousCount + 1);
        }
    };
</script>

```
每次点击按钮的时候，都会调用incrementClickCounter()函数，然后更新自动更新点击次数。



