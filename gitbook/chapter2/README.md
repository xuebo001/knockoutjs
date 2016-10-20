简单例子：

    <p>First name: <strong data-bind="text: firstName"></strong></p>
    <p>Last name: <strong data-bind="text: lastName"></strong></p>
    <p>First name: <input data-bind="value: firstName" /></p>
    <p>Last name: <input data-bind="value: lastName" /></p>
    <script>
    var myViewModel = {
    this.firstName = ko.observable("Bert");
    this.lastName = ko.observable("Bertington");
    }
    ko.applyBindings(myViewModel);
    </script>

* MVVM设计模式

    **Model**，用于存储你应用程序数据，这些数据表示你业务领域的对象和数据操作（例如：银行可以进行资金转账），
    并且独立于任何界面。当使用KO的时候，通常是使用Ajax向服务器请求数据来读写这个数据模型。
    
    **View Model**，纯粹用于描述数据内容和页面操作的数据模型。例如，如果你想实现一个列表编辑器，
    你的ViewModel（数据模型）就是项目清单对象和你所暴露出来的添加和删除列表项的方法。
    
    **View**，代表View Model状态的一个可见、互动的UI界面。

* Observable

    如上例子所示，我们通过将view model的属性声明成observable的，来实现当View Model发生变化时自动的更新UI界面的功能。
    它能够通知用户它的改变以及自动检测依赖关系。
    
    读取observable属性：`myViewModel.personName（）`
    
    设置observable属性：`myViewModel.personName（"Mary"）`
    
    同时设置多个observable属性：`myViewModel.personName（"Mary"）.personAge（50）` 链式语法

* applyBinding

    Knockout调用applyBindings激活myViewModel,这样来让data-bind属性生效（把myViewModel和View中的声明式绑定data-bind关联起来）。
    
    ko.applyBindings有两个参数，第一个参数是你想激活KO时用于声明式绑定的View Model对象，第二个参数（可选），来设置要使用data-bind属性的HTML元素或容器。比如：
    ```
    ko.applyBindings(myViewModel,document.getElementById('someElementId'))
    ```
    限制了只有ID为someElementId的元素才能激活使用KO功能,对于appViewModel






