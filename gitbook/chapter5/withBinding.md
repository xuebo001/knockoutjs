使用with binding来重新定义一个上下文绑定

```
<script type="text/javascript" src="knockout-2.2.0.js">
</script>
<h1 data-bind="text: city">
</h1>
<p data-bind="with: coords">
    Latitude:
    <span data-bind="text: latitude">
    </span>
    , Longitude:
    <span data-bind="text: longitude">
    </span>
</p>
<script type="text/javascript">
    ko.applyBindings({
        city: "London",
        coords: {
            latitude: 51.5001524,
            longitude: -0.1262362
        }
    });
</script>
```
这样我们在使用coords下的latitude和longitude的时候我们就不需要使用coords.latitude来调用了，
因为我们使用with:coords来指定了coords的上下文， coords下面的属性可以直接使用了。



