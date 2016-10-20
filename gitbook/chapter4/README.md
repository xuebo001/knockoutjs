让我们通过一个简单的例子来了解计算属性的用法：

```
<p>First name: <strong data-bind="text: firstName"></strong></p>
<p>Last name: <strong data-bind="text: lastName"></strong></p>
<p>full name: <strong data-bind="text: fullName"></strong></p>
<script>
var AppViewModel = function () { 
	this.firstName = ko.observable("Bert");
    	this.lastName = ko.observable("Bertington");
	this.fullName = ko.computed(function () {
              return this.firstName() + " " + this.lastName();
        }, this);
}
ko.applyBindings(new AppViewModel());
</script>

```
其中this代表AppViewModel，我们通过计算属性得到了全名


