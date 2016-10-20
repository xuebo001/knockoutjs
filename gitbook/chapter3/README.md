发现并响应一个对象的改变，用监控属性（observables）。发现并响应一个集合的变化，用监控属性数组（observableArray）

##### 初始化数组：

方式一：

        var myObservableArray = ko.observableArray(); （实例化了一个数组）
        myObservableArray.push('Somevalue');myObservableArray.push('Somevalue');

方式二：

        var anotherObservableArray = ko.observableArray([
        {name: "Bungle", type: "Bear" }, 
        {name: "George", type: "Hippo" },
        {name: "Zippy", type: "Unknown" }
        ]);  
          
##### 访问数组：

        alert('The length of the array is ' + observableArray().length);
        alert('The first element is ' + observableArray()[0]);
        
##### 常用的方法:

1. `myObservableArray.push('Some new value')`：增加一个新的元素

2. `myObservableArray.pop()`：删除一个元素，并返回其值

3. `myObservableArray.unshift('Some new value')`：在数组的开始处增加一个新的元素

4. `myObservableArray.shift()`：删除数组的第一个元素，并返回其值

5. `myObservableArray.reverse()`：反转数组的顺序

6. `myObservableArray.sort()`：数组排序。（默认情况下按照字母顺序或者数字的顺序进行排序）

7. `myObservableArray.splice()`：数组截取

8. `remove and removeAll`：移除数据

