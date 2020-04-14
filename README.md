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