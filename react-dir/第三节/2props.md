## 2. `props`
通过 this.props 可以获取传递给该组件的属性值，还可以通过定义 getDefaultProps 来指定默认属性值（这是ES5的写法，ES6定义组件的默认props可以直接写props）

下面几个是props的常用API：
- `this.props.children`
- `this.props.map`
- `this.props.filter`

**props是调用组件的时候传递进去的数据，一般用于组件树数据传递**

```
import React, { Component } from 'react';

class PropsDemo extends Component {
  props = {
    title: '这是默认的title属性值'
  }
  render(){
    console.log(this.props);

    return <b>{this.props.title}</b>
  }
}

export default PropsDemo;


// 组件调用方式
// <PropsDemo title="设置的标题" />
```