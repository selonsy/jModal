# jModal
a jquery plugin to encapsulation Alert/Confirm/Feedback actions with modal.

## Usage

### Dependence

* jQuery
* BootStrape

### Example

```javascript
//alert
DSModal.alert({ msg: "msg" });
DSModal.alert({ msg: "msg", type: false });
DSModal.alert({ msg: "msg", type: false, time: 5000 });

//confirm
DSModal.confirm({ msg: "msg" }).on(function () { console.log("success callback"); }, function () { console.log("fail callback"); });

//feedback
DSModal.feedback({ msg: "msg" }).on(function () { console.log("success callback"); }, function () { console.log("fail callback"); });

```

### Options

jModal can be configured using the following options.

1.alert  
* `msg` - The msg which will show.
* `type` - Base on the type of msg,show different style, default is `true`.
* `time` - The time of msg disappear, default is `2000ms`.  

2.confirm  
* `msg` - The msg which will show.
* `btnok` - The name of confirm button, default is `确定`.
* `btncl` - The name of cancel button, default is `取消`.  

3.feedback  
* `title` - The title of modal dialog.
* `btnok` - The name of confirm button, default is `确定`.
* `btncl` - The name of cancel button, default is `取消`.
* `placeholder` - The default msg of textarea.

### API

jModal provide following methods to allow you control your msg.

* `DSModal.alert(options)` - Show tips msg with different styles.
* `DSModal.confirm(options).on(successCall,cancelCall)` - Show confirm msg with ok&cancel button.
* `DSModal.feedback(options).on(successCall,cancelCall)` -  Show modal dialog,such as message board or feedback.

## Licence

[MIT](http://opensource.org/licenses/MIT)
