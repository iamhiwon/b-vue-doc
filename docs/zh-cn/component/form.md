#   

>  。


###  代码演示

```
 
```

### API
参数|说明|类型|默认值|版本
--|--|--|--|--
form|经 Form.create() 包装过的组件会自带 this.form 属性，如果使用 template 语法，可以使用 this.$form.createForm(this, options)|object|无|
hideRequiredMark|隐藏所有表单项的必选标记|Boolean|false|
labelAlign|label 标签的文本对齐方式|'left' | 'right'|'right'|1.5.0
layout|表单布局|'horizontal'|'vertical'|'inline'|'horizontal'|
labelCol|label 标签布局，同 <Col> 组件，设置 span offset 值，如 {span: 3, offset: 12} 或 sm: {span: 3, offset: 12}|object||
wrapperCol|需要为输入控件设置布局样式时，使用该属性，用法同 labelCol|object||
selfUpdate|自定义字段更新逻辑，说明见下，需 1.3.17 版本以上|boolean|false|1.3.17
colon|配置 Form.Item 的 colon 的默认值 (只有在属性 layout 为 horizontal 时有效)|boolean|true|1.5.0



事件名称|说明|回调参数
--|--|--
submit|数据验证成功后回调事件|Function(e:Event)


参数|说明|类型
--|--|--
props|仅仅支持 Form.create({})(CustomizedForm)的使用方式，父组件需要映射到表单项上的属性声明(和vue 组件 props 一致)|{}
mapPropsToFields|把父组件的属性映射到表单项上（如：把 Redux store 中的值读出），需要对返回值中的表单域数据用 Form.createFormField 标记，如果使用$form.createForm 创建收集器，你可以将任何数据映射到 Field 中，不受父组件约束|(props) => ({ [fieldName]: FormField { value } })
name|设置表单域内字段 id 的前缀|-
validateMessages|默认校验信息，可用于把默认错误信息改为中文等，格式与 newMessages 返回值一致|Object { [nested.path]: String }
onFieldsChange|当 Form.Item 子节点的值发生改变时触发，可以把对应的值转存到 Redux store|Function(props, fields)
onValuesChange|任一表单域的值发生改变时的回调|(props, values) => void



方法|说明|类型
--|--|--
getFieldDecorator|用于和表单进行双向绑定，单文件 template 可以使用指令v-decorator进行绑定，详见下方描述|
getFieldError|获取某个输入控件的 Error|Function(name)
getFieldsError|获取一组输入控件的 Error ，如不传入参数，则获取全部组件的 Error|Function([names: string[]])
getFieldsValue|获取一组输入控件的值，如不传入参数，则获取全部组件的值|Function([fieldNames: string[]])
getFieldValue|获取一个输入控件的值|Function(fieldName: string)
isFieldsTouched|判断是否任一输入控件经历过 getFieldDecorator 或 v-decorator 的值收集时机 options.trigger|(names?: string[]) => boolean
isFieldTouched|判断一个输入控件是否经历过 getFieldDecorator 或 v-decorator 的值收集时机 options.trigger|(name: string) => boolean
isFieldValidating|判断一个输入控件是否在校验状态|Function(name)
resetFields|重置一组输入控件的值（为 initialValue）与状态，如不传入参数，则重置所有组件|Function([names: string[]])
setFields|设置一组输入控件的值与错误状态。|Function({ [fieldName]: { value: any, errors: [Error] } })
setFieldsValue|设置一组输入控件的值|Function({ [fieldName]: value })
validateFields|校验并获取一组输入域的值与 Error，若 fieldNames 参数为空，则校验全部组件|Function([fieldNames: string[]], [options: object], callback: Function(errors, values))
validateFieldsAndScroll|与 validateFields 相似，但校验完后，如果校验不通过的菜单域不在可见范围内，则自动滚动进可见范围|参考 validateFields



参数|说明|类型|默认值
--|--|--|--
options.first|若为 true，则每一表单域的都会在碰到第一个失败了的校验规则后停止校验|boolean|false
options.firstFields|指定表单域会在碰到第一个失败了的校验规则后停止校验|String[]|[]
options.force|对已经校验过的表单域，在 validateTrigger 再次被触发时是否再次校验|boolean|false
options.scroll|定义 validateFieldsAndScroll 的滚动行为，详细配置见 dom-scroll-into-view config|Object|{}



参数|说明|类型|默认值
--|--|--|--
id|必填输入控件唯一标志。支持嵌套式的写法。|string|
options.getValueFromEvent|可以把 onChange 的参数（如 event）转化为控件的值|function(..args)|reference
options.initialValue|子节点的初始值，类型、可选值均由子节点决定(注意：由于内部校验时使用 === 判断是否变化，建议使用变量缓存所需设置的值而非直接使用字面量)||
options.normalize|转换默认的 value 给控件，一个选择全部的例子|function(value, prevValue, allValues): any|-
options.preserve|即便字段不再使用，也保留该字段的值|boolean|false
options.rules|校验规则，参考下方文档|object[]|
options.trigger|收集子节点的值的时机|string|'change'
options.validateFirst|当某一规则校验不通过时，是否停止剩下的规则的校验|boolean|false
options.validateTrigger|校验子节点值的时机|string|string[]|'change'
options.valuePropName|子节点的值的属性，如 Switch 的是 'checked'|string|'value'



参数|说明|类型|默认值|版本
--|--|--|--|--
colon|配合 label 属性使用，表示是否显示 label 后面的冒号|boolean|true|
extra|额外的提示信息，和 help 类似，当需要错误信息和提示文案同时出现时，可以使用这个。|string|slot||
hasFeedback|配合 validateStatus 属性使用，展示校验状态图标，建议只配合 Input 组件使用|boolean|false|
help|提示信息，如不设置，则会根据校验规则自动生成|string|slot||
htmlFor|设置子元素 label htmlFor 属性|string||1.5.0
label|label 标签的文本|string|slot||
labelCol|label 标签布局，同 <Col> 组件，设置 span offset 值，如 {span: 3, offset: 12} 或 sm: {span: 3, offset: 12}|object||
labelAlign|标签文本对齐方式|'left' | 'right'|'right'|1.5.0
required|是否必填，如不设置，则会根据校验规则自动生成|boolean|false|
validateStatus|校验状态，如不设置，则会根据校验规则自动生成，可选：'success' 'warning' 'error' 'validating'|string||
wrapperCol|需要为输入控件设置布局样式时，使用该属性，用法同 labelCol|object||
selfUpdate|自定义字段更新逻辑，你可以通过 Form 的 selfUpdate 进行统一设置。当和 Form 同时设置时，以 Item 为准。 说明见下 需 1.3.17 版本以上|boolean|false|1.3.17



参数|说明|类型|默认值
--|--|--|--
enum|枚举类型|string|-
len|字段长度|number|-
max|最大长度|number|-
message|校验文案|string|-
min|最小长度|number|-
pattern|正则表达式校验|RegExp|-
required|是否必选|boolean|false
transform|校验前转换字段值|function(value) => transformedValue:any|-
type|内建校验类型，可选项|string|'string'
validator|自定义校验（注意，callback 必须被调用）|function(rule, value, callback)|-
whitespace|必选时，空格是否会被视为错误|boolean|false





 


### 事件

 

