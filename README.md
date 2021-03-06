# d3-learn
学习d3

## 地址

[d3-tutorial](https://www.tutorialsteacher.com/d3js)



D3：Data-Driven Documents

SVG：Scalable Vector Graphics


## 02-dom-selection
[选择器](https://www.w3.org/TR/selectors-3/)

## 03-dom-manipulation

在使用`d3.select()`和`d3.selectAll()`选择元素后，可以使用以下方法：

| 方法                       | 描述                                                         |
| -------------------------- | ------------------------------------------------------------ |
| text('content')            | Gets or sets the text of the selected element                |
| append('element name')     | Adds an element inside the selected element but just before the end of the selected element. |
| insert('element name')     | Inserts a new element in the selected element                |
| remove()                   | Inserts a new element in the selected element                |
| html('content')            | Gets or sets the inner HTML of selected element              |
| attr('name', 'value')      | Gets or sets an attribute on the selected element.           |
| property('name', 'value')  | Gets or sets an attribute on the selected element.           |
| style('name', 'value')     | Gets or sets the style of the selected element               |
| classed('css class', bool) | Gets, adds or removes a css class from the selection         |

- 没发现`append`和`insert`的区别
- `attr()`和`property()`的区别：元素某些属性无法使用`attr()`设置，如：**checked property of checkbox or radio button**，可以使用`property()`方法进行设置

attr和property的区别：

1. attribute是HTML标签上的属性，**它的值只能是字符串**。attribute就是html元素自带的属性，如id、class、title等。
2. property是DOM中的属性。property是DOM元素作为对象，其自身属性，如childNodes、firstChild、className等。`attributes`（NameNodeMap）是DOM对象的一个property，在html元素上自定义的某些属性都会保存到这个attributes里

```js
// html
<input type="radio" checked="anything" id="radio">
// js
const radio = document.getElementById('radio')
radio.getAttribute('checked') // anything
radio.checked // true
```



## 06-event-handling

```js
d3.selection.on(type, [, listener[, capture]])
```

- 事件默认是冒泡。通过设置第三个参数capture来改变。



## 10-create-svg-elements

Each SVG element has it's own properties - which includes both geometry and style properties. All properties can be set as attributes but generally, we provide geometry properties as attributes and styling properties as styles.

The default SVG color is black fill width no stroke.

| style attribute | Description                                                  |
| --------------- | ------------------------------------------------------------ |
| fill            | This is the fill color for your element. It can be color name, hex value, or RGB or RGBA values. |
| stroke          | This is the stroke color. Like our line example above, we can specify a color for our element. |
| stroke-width    | Stroke width specifies the width of our line or boundary. This is in pixels. |
| opacity         | Opacity will specify an opacity/transparency number. 0 is completely transparent and 1 is completely opaque. |
| font-family     | For text elements, we can specify the font-family. This works like CSS. |
| font-size       | We can also specify the font-size for text elements.         |

## 12-scales

Domain: Domain denotes minimum and maximum values of your **input** data.

Range: Range is the **output** range that you would like your input values to map to.