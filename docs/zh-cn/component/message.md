#   

>  。


###  代码演示

```
 
```

### API
参数	说明	类型	默认值
content	提示内容	string| VNode |(h) => VNode	-
duration	自动关闭的延时，单位秒。设为 0 时不自动关闭。	number	3
onClose	关闭时触发的回调函数	Function	-


参数	说明	类型	默认值	版本
content	提示内容	string| VNode |(h) => VNode	-	
duration	自动关闭的延时，单位秒。设为 0 时不自动关闭。	number	3	
onClose	关闭时触发的回调函数	Function	-	
icon	自定义图标	string| VNode |(h) => VNode	-	
key	当前提示的唯一标志	string|number	-	1.5.0


参数	说明	类型	默认值
duration	默认自动关闭延时，单位秒	number	3
getContainer	配置渲染节点的输出位置	() => HTMLElement	() => document.body
maxCount	最大显示数, 超过限制时，最早的消息会被自动关闭	number	-
top	消息距离顶部的位置	string	24px

 


### 事件

 

