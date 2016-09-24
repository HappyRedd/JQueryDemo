# JQueryDemo
JQueryDemo
### on()的多事件绑定
基本用法：
```
.on( events [, selector ] [, data ] )
```
最常见的给元素绑定一个点击事件，对比下一下快捷方式与on方式的不同:
```
$("#elem").click(function(){})  //快捷方式
$("#elem").on('click',function(){}) //on方式
```
最大的不同点就是on是可以自定义事件名，当然不仅仅只是 如此，继续往下看如此付：
** 多个事件绑定同一个函数 **
```
 $("#elem").on("mouseover mouseout",function(){ });
```
通过空格分离，传递不同的事件名，可以同时绑定多个事件
**  多个事件绑定不同函数**
```
$("#elem").on({
    mouseover:function(){},  
    mouseout:function(){},
});
```
通过空格分离，传递不同的事件名，可以同时绑定多个事件，每一个事件执行自己的回调方法
** 将数据传递到处理程序**
```
function greet( event ) {
  alert( "Hello " + event.data.name ); //Hello Redd
}
$( "button" ).on( "click", {
  name: "Redd"
}, greet );
```
可以通过第二参数（对象），当一个事件被触发时，要传递给事件处理函数的
以上都是on方法基本用法，具体的使用方法[Jquery.on.Demo](https://github.com/HappyRedd/JQueryDemo/edit/master/Jquery.on.Demo.html)
