#   

>  。


###  代码演示

```
 
```

### API
参数	说明	类型	默认值
disabled	菜单是否禁用	boolean	-
getPopupContainer	菜单渲染父节点。默认渲染到 body 上，如果你遇到菜单滚动定位问题，试试修改为滚动的区域，并相对其定位。	Function(triggerNode)	() => document.body
overlay(slot-scope)	菜单	Menu	-
overlayClassName	下拉根元素的类名称	string	-
overlayStyle	下拉根元素的样式	object	-
placement	菜单弹出位置：bottomLeft bottomCenter bottomRight topLeft topCenter topRight	String	bottomLeft
trigger	触发下拉的行为, 移动端不支持 hover	Array<click|hover|contextmenu>	['hover']
visible(v-model)	菜单是否显示	boolean	-

 


### 事件
事件名称	说明	回调参数
visibleChange	菜单显示状态改变时调用，参数为 visible	function(visible)
 
参数	说明	类型	默认值	版本
disabled	菜单是否禁用	boolean	-	
icon	右侧的 icon	VNode | slot	-	1.5.0
overlay(slot-scope)	菜单	Menu	-	
placement	菜单弹出位置：bottomLeft bottomCenter bottomRight topLeft topCenter topRight	String	bottomLeft	
size	按钮大小，和 Button 一致	string	'default'	
trigger	触发下拉的行为	Array<click|hover|contextmenu>	['hover']	
type	按钮类型，和 Button 一致	string	'default'	
visible(v-model)	菜单是否显示	boolean	-	


事件名称	说明	回调参数
click	点击左侧按钮的回调，和 Button 一致	Function
visibleChange	菜单显示状态改变时调用，参数为 visible	function(visible)







