使用此功能可以方便我们循环遍历输出某个数组、集合中的内容。

* 循环遍历输出数组:

    ```
    <script type="text/javascript" src="knockout-2.2.0.js"></script>
     <table> 
         <thead> 
             <tr><th>First name</th><th>Last name</th></tr> 
         </thead> 
         <tbody data-bind="foreach: people"> 
             <tr> 
                 <td data-bind="text: firstName"></td> 
                 <td data-bind="text: lastName"></td> 
             </tr> 
         </tbody> 
     </table> 
     <script type="text/javascript">
         ko.applyBindings({
             people: [
                 { firstName: 'Bert', lastName: 'Bertington' },
                 { firstName: 'Charles', lastName: 'Charlesforth' },
                 { firstName: 'Denise', lastName: 'Dentiste' }
             ]
         });
     </script>
    
    ```
    
* 动态增加和删除遍历节点

    ```
    <script type="text/javascript" src="knockout-2.2.0.js"></script>
     <h4>People</h4> 
     <ul data-bind="foreach: people"> 
    //<ul data-bind="foreach: { data: people, as: 'peo' }">
         <li> 
             Name at position <span data-bind="text: $index"> </span>: 
             <span data-bind="text: name"> </span> 
             //<span data-bind="text: $data"> </span>
             <a href="#" data-bind="click: $parent.removePerson">Remove</a> 
         </li> 
     </ul> 
     <button data-bind="click: addPerson">Add</button> 
     <script type="text/javascript">
         function AppViewModel() {
             var self = this;
             self.people = ko.observableArray([
             { name: 'Bert' },
             { name: 'Charles' },
             { name: 'Denise' }
         ]);
             self.addPerson = function () {
                 self.people.push({ name: "New at " + new Date() });
             };
             self.removePerson = function () {
                 self.people.remove(this);
             }
         }
         ko.applyBindings(new AppViewModel());
     </script>
    
    ```
    
$index来表示我们数组的下标,，$parent来使用foreach循环体之外的属性
可以使用$data来代替数组中的元素，同时我们也可以使用as来为我们要遍历的元素起一个别名


