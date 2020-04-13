#   

>  。


###  代码演示

```
 
```

### API
参数	说明	类型	默认值
dateCellRender	作用域插槽，用来自定义渲染日期单元格，返回内容会被追加到单元格,	function(date: moment)	无
dateFullCellRender	作用域插槽，自定义渲染日期单元格，返回内容覆盖单元格	function(date: moment)	无
defaultValue	默认展示的日期	moment	默认日期
disabledDate	不可选择的日期	(currentDate: moment) => boolean	无
fullscreen	是否全屏显示	boolean	true
locale	国际化配置	object	默认配置
mode	初始模式，month/year	string	month
monthCellRender	作用域插槽，自定义渲染月单元格，返回内容会被追加到单元格	function(date: moment)	无
monthFullCellRender	作用域插槽，自定义渲染月单元格，返回内容覆盖单元格	function(date: moment)	无
validRange	设置可以显示的日期	[moment, moment]	无
value(v-model)	展示日期	moment	当前日期
headerRender	自定义头部内容	function(object:{value: moment, type: string, onChange: f(), onTypeChange: f()}) | slot-scope	-
 

事件名称	说明	回调参数
panelChange	日期面板变化回调	function(date: moment, mode: string)
select	点击选择日期回调	function(date: moment）
change	日期变化时的回调, 面板变化有可能导致日期变化	function(date: moment）

 
 
 

### 事件

 

