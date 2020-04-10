#   

>  。


###  代码演示

```
 
```

### API
参数	说明	类型	默认值	版本
tableLayout	表格元素的 table-layout 属性，设为 fixed 表示内容不会影响列的布局	- | 'auto' | 'fixed'	无
固定表头/列或使用了 column.ellipsis 时，默认值为 fixed	1.5.0
bordered	是否展示外边框和列边框	boolean	false	
childrenColumnName	指定树形结构的列名	string[]	children	
columns	表格列的配置描述，具体项见下表	array	-	
components	覆盖默认的 table 元素	object	-	
dataSource	数据数组	any[]		
defaultExpandAllRows	初始时，是否展开所有行	boolean	false	
defaultExpandedRowKeys	默认展开的行	string[]	-	
expandedRowKeys	展开的行，控制属性	string[]	-	
expandedRowRender	额外的展开行	Function(record, index, indent, expanded):VNode | slot="expandedRowRender" slot-scope="record, index, indent, expanded"	-	
expandIcon	自定义展开图标	Function(props):VNode | slot="expandIcon" slot-scope="props"	-	
expandRowByClick	通过点击行来展开子行	boolean	false	
expandIconColumnIndex	展开的图标显示在哪一列，如果没有 rowSelection，默认显示在第一列，否则显示在选择框后面	number		
footer	表格尾部	Function(currentPageData)|slot-scope		
indentSize	展示树形数据时，每层缩进的宽度，以 px 为单位	number	15	
loading	页面是否加载中	boolean|object	false	
locale	默认文案设置，目前包括排序、过滤、空数据文案	object	filterConfirm: '确定'
filterReset: '重置'
emptyText: '暂无数据'

pagination	分页器，参考配置项或 pagination文档，设为 false 时不展示和进行分页	object		
rowClassName	表格行的类名	Function(record, index):string	-	
rowKey	表格行 key 的取值，可以是字符串或一个函数	string|Function(record):string	'key'	
rowSelection	列表项是否可选择，配置项	object	null	
scroll	设置横向或纵向滚动，也可用于指定滚动区域的宽和高，建议为 x 设置一个数字，如果要设置为 true，需要配合样式 .ant-table td { white-space: nowrap; }	{ x: number | true, y: number }	-	
showHeader	是否显示表头	boolean	true	
size	表格大小	default | middle | small	default	
title	表格标题	Function(currentPageData)|slot-scope		
customHeaderRow	设置头部行属性	Function(column, index)	-	
customRow	设置行属性	Function(record, index)	-	
getPopupContainer	设置表格内各类浮层的渲染节点，如筛选菜单	(triggerNode) => HTMLElement	() => TableHtmlElement	1.5.0



事件名称	说明	回调参数
expandedRowsChange	展开的行变化时触发	Function(expandedRows)
change	分页、排序、筛选变化时触发	Function(pagination, filters, sorter, { currentDataSource })
expand	点击展开图标时触发	Function(expanded, record)



参数	说明	类型	默认值	版本
align	设置列内容的对齐方式	'left' | 'right' | 'center'	'left'	
ellipsis	超过宽度将自动省略，暂不支持和排序筛选一起使用。
设置为 true 时，表格布局将变成 tableLayout="fixed"。	boolean	false	1.5.0
colSpan	表头列合并,设置为 0 时，不渲染	number		
dataIndex	列数据在数据项中对应的 key，支持 a.b.c 的嵌套写法	string	-	
defaultFilteredValue	默认筛选值	string[]	-	1.5.0
filterDropdown	可以自定义筛选菜单，此函数只负责渲染图层，需要自行编写各种交互	VNode | slot-scope	-	
filterDropdownVisible	用于控制自定义筛选菜单是否可见	boolean	-	
filtered	标识数据是否经过过滤，筛选图标会高亮	boolean	false	
filteredValue	筛选的受控属性，外界可用此控制列的筛选状态，值为已筛选的 value 数组	string[]	-	
filterIcon	自定义 fiter 图标。	VNode | (filtered: boolean, column: Column) => vNode |slot |slot-scope	false	
filterMultiple	是否多选	boolean	true	
filters	表头的筛选菜单项	object[]	-	
fixed	列是否固定，可选 true(等效于 left) 'left' 'right'	boolean|string	false	
key	Vue 需要的 key，如果已经设置了唯一的 dataIndex，可以忽略这个属性	string	-	
customRender	生成复杂数据的渲染函数，参数分别为当前行的值，当前行数据，行索引，@return 里面可以设置表格行/列合并,可参考 demo 表格行/列合并	Function(text, record, index) {}|slot-scope	-	
sorter	排序函数，本地排序使用一个函数(参考 Array.sort 的 compareFunction)，需要服务端排序可设为 true	Function|boolean	-	
sortOrder	排序的受控属性，外界可用此控制列的排序，可设置为 'ascend' 'descend' false	boolean|string	-	
sortDirections	支持的排序方式，取值为 'ascend' 'descend'	Array	['ascend', 'descend']	1.5.0
title	列头显示文字	string|slot	-	
width	列宽度	string|number	-	
customCell	设置单元格属性	Function(record, rowIndex)	-	
customHeaderCell	设置头部单元格属性	Function(column)	-	
onFilter	本地模式下，确定筛选的运行函数, 使用 template 或 jsx 时作为filter事件使用	Function	-	
onFilterDropdownVisibleChange	自定义筛选菜单可见变化时调用，使用 template 或 jsx 时作为filterDropdownVisibleChange事件使用	function(visible) {}	-	
slots	使用 columns 时，可以通过该属性配置支持 slot 的属性，如 slots: { filterIcon: 'XXX'}	object	-	
scopedSlots	使用 columns 时，可以通过该属性配置支持 slot-scope 的属性，如 scopedSlots: { customRender: 'XXX'}	object	-	



参数	说明	类型	默认值
title	列头显示文字	string|slot	-
slots	使用 columns 时，可以通过该属性配置支持 slot 的属性，如 slots: { title: 'XXX'}	object	-


参数	说明	类型	默认值
position	指定分页显示的位置	'top' | 'bottom' | 'both'	'bottom'


参数	说明	类型	默认值
columnWidth	自定义列表选择框宽度	string|number	-
columnTitle	自定义列表选择框标题	string|VNode	-
fixed	把选择框列固定在左边	boolean	-
getCheckboxProps	选择框的默认属性配置	Function(record)	-
hideDefaultSelections	去掉『全选』『反选』两个默认选项	boolean	false
selectedRowKeys	指定选中项的 key 数组，需要和 onChange 进行配合	string[]	[]
selections	自定义选择配置项, 设为 true 时使用默认选择项	object[]|boolean	true
type	多选/单选，checkbox or radio	string	checkbox
onChange	选中项发生变化时的回调	Function(selectedRowKeys, selectedRows)	-
onSelect	用户手动选择/取消选择某列的回调	Function(record, selected, selectedRows, nativeEvent)	-
onSelectAll	用户手动选择/取消选择所有列的回调	Function(selected, selectedRows, changeRows)	-
onSelectInvert	用户手动选择反选的回调	Function(selectedRows)	-



参数	说明	类型	默认值	版本
x	设置横向滚动，也可用于指定滚动区域的宽和高，可以设置为像素值，百分比，true 和 'max-content'	number | true	-	
y	设置纵向滚动，也可用于指定滚动区域的宽和高，可以设置为像素值，百分比，true 和 'max-content'	number | true	-	
scrollToFirstRowOnChange	当分页、排序、筛选变化后是否滚动到表格顶部	boolean	-	1.5.0


参数	说明	类型	默认值
key	Vue 需要的 key，建议设置	string	-
text	选择项显示的文字	string|VNode	-
onSelect	选择项点击回调	Function(changeableRowKeys)	-



 


### 事件

 

