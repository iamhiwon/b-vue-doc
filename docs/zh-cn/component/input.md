#   

>  。


###  代码演示

```
 
```

### API
参数|说明|类型|默认值|版本
--|--|--|--|--
addonAfter|带标签的 input，设置后置标签|string|slot||
addonBefore|带标签的 input，设置前置标签|string|slot||
defaultValue|输入框默认内容|string||
disabled|是否禁用状态，默认为 false|boolean|false|
id|输入框的 id|string||
maxLength|最大长度|number||1.5.0
prefix|带有前缀图标的 input|string|slot||
size|控件大小。注：标准表单内的输入框大小限制为 large。可选 large default small|string|default|
suffix|带有后缀图标的 input|string|slot||
type|声明 input 类型，同原生 input 标签的 type 属性，见：MDN(请直接使用 Input.TextArea 代替 type="textarea")。|string|text|
value(v-model)|输入框内容|string||
allowClear|可以点击清除图标删除内容|boolean||


事件名称|说明|回调参数
--|--|--
change|输入框内容变化时的回调|function(e)
pressEnter|按下回车的回调|function(e)



参数|说明|类型|默认值|版本
--|--|--|--|--
autosize|自适应内容高度，可设置为 true|false 或对象：{ minRows: 2, maxRows: 6 }|boolean|object|false|
defaultValue|输入框默认内容|string||
value(v-model)|输入框内容|string||
allowClear|可以点击清除图标删除内容|boolean||1.5.0


事件名称|说明|回调参数
--|--|--
pressEnter|按下回车的回调|function(e)


参数|说明|类型|默认值|版本
--|--|--|--|--
enterButton|是否有确认按钮，可设为按钮文字。该属性会与 addon 冲突。|boolean|slot|false|
loading|搜索 loading|boolean||1.5.0


事件名称|说明|回调参数
--|--|--
search|点击搜索或按下回车键时的回调|function(value, event)


参数|说明|类型|默认值
--|--|--|--
compact|是否用紧凑模式|boolean|false
size|Input.Group 中所有的 Input 的大小，可选 large default small|string|default



 


### 事件

 

