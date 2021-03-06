# TagPicker 标签输入选择器

以标签的方式进行多选，同时支持新增选项

* `<TagPicker>`

## 获取组件

```js
import { TagPicker } from 'rsuite';
```

## 演示

<!--{demo}-->

## Props


### `<TagPicker>`

| 属性名称             | 类型`(默认值)`                                                   | 描述                                  |
| -------------------- | ---------------------------------------------------------------- | ------------------------------------- |
| classPrefix          | string `('picker')`                                              | 组件 CSS 类的前缀                     |
| creatable            | boolean `(true)`                                                 | 设置可以新建选项                      |
| data \*              | Array&lt;[DataItemType](#DataItemType)&gt;                       | 组件数据                              |
| cacheData            | Array&lt;[DataItemType](#DataItemType)&gt;                       | 当异步搜索时，用于缓存 `value` 的选项 |
| disabled             | boolean                                                          | 禁用组件                              |
| disabledItemValues   | Array&lt;string&gt;                                              | 禁用选项                              |
| groupBy              | string                                                           | 设置分组条件在 `data` 中的 `key`      |
| valueKey             | string `('value')`                                               | 设置选项值在 `data` 中的 `key`        |
| labelKey             | string `('label')`                                               | 设置选项显示内容在 `data` 中的 `key`  |
| value                | Array&lt;string&gt;                                              | 设置值 `受控`                         |
| defaultValue         | Array&lt;string&gt;                                              | 设置默认值 `非受控`                   |
| height               | number `(320)`                                                   | 设置 Dropdown 的高度                  |
| onChange             | (value:string, event)=>void                                      | `value` 发生改变时的回调函数          |
| onSelect             | (value:string, item: DataItemType , event)=>void                 | 选项被点击选择后的回调函数            |
| onSearch             | (searchKeyword:string, event)=>void                              | 搜索的回调函数                        |
| onOpen               | ()=>void                                                         | 打开回调函数                          |
| onClose              | ()=>void                                                         | 关闭回调函数                          |
| onGroupTitleClick    | (event)=>void                                                    | 点击分组标题的回调函数                |
| placeholder          | React.Node `('Select')`                                          | 占位符                                |
| renderValue          | (value: Array&lt;any&gt;, items: Array&lt;any&gt;) => React.Node | 自定义被选中的选项                    |
| renderMenuItem       | (label:React.Node, item: DataItemType)=>React.Node               | 自定义选项                            |
| renderMenuGroup      | (groupTitle:React.Node, item:DataItemType)=>React.Node           | 自定义选项组                          |
| renderExtraFooter    | ()=>React.Node                                                   | 自定义页脚内容                        |
| searchable           | boolean `(true)`                                                 | 可以搜索                              |
| cleanable            | boolean `(true)`                                                 | 可以清除                              |
| placement            | enum: [Placement](#Placement)`('bottomLeft')`                    | 位置                                  |
| menuClassName        | string                                                           | 应用于菜单 DOM 节点的 css class       |
| menuStyle            | Object                                                           | 应用于菜单 DOM 节点的 style           |
| container            | HTMLElement or (() => HTMLElement)                               | 设置渲染的容器                        |
| toggleComponentClass | React.ElementType `('a')`                                        | 为组件自定义元素类型                  |

## Types



### DataItemType

```ts
type DataItemType = {
  value: any;
  label: React.Node;
  groupBy?: string;
};
```
