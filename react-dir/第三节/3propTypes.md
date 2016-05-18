## 3. `propTypes`

通过指定 propTypes 可以校验props属性值的类型，校验可提升开发者体验，用于约定统一的接口规范。

```
import React, { Component, PropTypes } from 'react';

class PropTypesDemo extends Component {

  render(){
    return <b>{this.props.title}</b>
  }
}

PropTypesDemo.defaultProps= {
  title: '我是默认的title'
}

PropTypesDemo.propTypes = {
  title: PropTypes.string.isRequired
}

export default PropTypesDemo;

```
