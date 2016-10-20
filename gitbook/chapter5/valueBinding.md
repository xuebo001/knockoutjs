value绑定是关联DOM元素的值到view model的属性上。主要是用在表单控件`<input>`，`<select>`和`<textarea>`上。

```
<p>
    Login name:
    <input data-bind="value: userName" />
</p>
<p>
    Password:
    <input type="password" data-bind="value: userPassword" />
</p>
<script type="text/javascript">
    var viewModel = {
        userName: ko.observable(""),
        // Initially blank  userPassword: ko.observable("abc"), // Prepopulate    };
        
</script>

```

注：不管什么时候，只要你更新了元素的值，那 KO都会将view model对应的属性值自动更新。默认情况下当用户离开焦点（例如onchange事件）的时候，KO才更新这个值，但是你可以通过第2个参数valueUpdate来特别指定改变值的时机，例如：

`<input class="form-control" data-bind='value: itemToAdd, valueUpdate:"afterkeydown"'/>`

可选值：

“change”（默认值） - 当失去焦点的时候更新view model的值，或者是`<select> `元素被选择的时候。

“keyup” – 当用户敲完一个字符以后立即更新view model。

“keypress” – 当用户正在敲一个字符但没有释放键盘的时候就立即更新view model。不像 keyup，这个更新和keydown是一样的。

“afterkeydown” – 当用户开始输入字符的时候就更新view model。主要是捕获浏览器的keydown事件或异步handle事件。





