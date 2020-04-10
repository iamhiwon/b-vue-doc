#   

>  。


###  代码演示

```
 
```

### API
参数	说明	类型	可选值	默认值
itemRender	自定义链接函数，和 vue-router 配置使用， 也可使用 slot="itemRender" 和 slot-scope="props"	({route, params, routes, paths, h}) => vNode		-
params	路由的参数	object		-
routes	router 的路由栈信息	routes[]		-
separator	分隔符自定义	string|slot		'/'
 
参数	参数	类型	默认值	版本
href	链接的目的地	string	-	1.5.0
overlay	下拉菜单的内容	Menu | () => Menu	-	1.5.0


### 事件
事件名称	说明	回调参数	版本
click	单击事件	(e:MouseEvent)=>void
 

