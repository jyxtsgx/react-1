## 3. `使用 CHILDREN 组合`

自定义组件中可以通过 this.props.children 访问自定义组件的子节点
```
'use strict';

import React, { Component } from 'react';

// 定义一个组件，通过React.Children 拿到组件里面的子元素
class ListComponent extends Component {
  render(){
    return <ul>
      {
        React.Children.map( this.props.children, function(c){
          return <li>{c}</li>;
        })
      }
    </ul>
  }
}

class UseChildrenComponent extends Component {
  render(){
    return (
      <ListComponent>
        <a href="#">Facebook</a>
        <a href="#">Google</a>
        <a href="#">SpaceX</a>
      </ListComponent>
    )
  }
}

export default UseChildrenComponent;

```
