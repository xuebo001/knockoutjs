event绑定,大部分情况下是用在keypress，mouseover和mouseout上。

```html
<div>
    <div data-bind="event: { mouseover: enableDetails, mouseout: disableDetails }">
        Mouse over me
    </div>
    <div data-bind="visible: detailsEnabled">
        Details
    </div>
</div>
<script type="text/javascript">
    var viewModel = {
        detailsEnabled: ko.observable(false),
        enableDetails: function() {
            this.detailsEnabled(true);
        },
        disableDetails: function() {
            this.detailsEnabled(false);
        }
    };
</script>

```




