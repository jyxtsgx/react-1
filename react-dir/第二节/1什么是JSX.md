
## 1. `什么是 JSX`

类似 xml 的语法，用来描述组件树
```
var HelloMessage = React.createClass({
  render: function() {
    return <div>Hello {this.props.name}</div>;
  }
});

React.render(<HelloMessage name="John" />, mountNode);
```

JSX是可选的，并不强制要求使用。如果不用JSX，用React提供的API写的话，应该是这样的，直接调用React的API来定义组件和DOM元素。

```

var HelloMessage = React.createClass({
  displayName: "HelloMessage",
  render: function() {
    return React.createElement("div", null, "Hello ", this.props.name);
  }
});

React.render(React.createElement(HelloMessage, {name: "John"}), mountNode);
```