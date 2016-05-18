## 2. `一个简单的React组件及其渲染`

React组件通过一个 render() 方法，接受输入的参数并返回展示的对象。 以下这个例子使用了JSX，它类似于XML的语法。输入的参数通过 render() 传入组件后，将存储在this.props

`ES5 写法`
```
var React = require('react');
var ReactDOM = require('react-dom');

// 定义组件
var HelloMessage = React.createClass({
  render: function() {
    return <div> React，我们来了... </div>;
  }
});

// 组件渲染
ReactDOM.render(<HelloMessage />, rootElement);
```

`ES6 写法`
```
import React, { Component } from 'react';
import { render } from 'react-dom';

// 定义组件
class SimpleComponent extends Component {
  render(){
    return <div> React，我们来了... </div>;
  }
}

// 组件渲染
render(<HelloMessage />, rootElement);
```