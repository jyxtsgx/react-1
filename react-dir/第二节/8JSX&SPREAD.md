## 8. `JSX SPREAD`

可以通过 `{...obj}` 来批量设置一个对象的键值对到组件的属性

```
import React, { Component } from 'react';

class SpreadDemo extends Component {
  componentWillMount(){
    console.log(this.props);
  }
  render(){
    return <h1> {this.props.name} is a {this.props.type} </h1>;
  }
}

export default SpreadDemo;

```
