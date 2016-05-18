## 2. `用high-order component的方式实现`

```
import React, { Component } from 'react';

let Mixin = MixinComponent => class extends Component {
  constructor() {
    super();
    this.state = { val: 0 };
    this.update = this.update.bind(this);
  }
  update(){
    this.setState({val: this.state.val + 1});
  }
  componentWillMount(){
    console.log('will mount...')
  }
  render(){
    return (
      <MixinComponent
        update={this.update}
        {...this.state}
        {...this.props}
       />
    )
  }
  componentDidMount(){
    console.log('mounted...')
  }
}

const Button = (props) => {
  return (
    <button onClick={props.update}>
      {props.txt} - {props.val}
    </button>
  )
}

const Label = (props) => {
  return (
    <label onMouseMove={props.update}>
      {props.txt} - {props.val}
    </label>
  )
}

let ButtonMixed = Mixin(Button);
let LabelMixed = Mixin(Label);

class Mixins extends Component {
  render(){
    return (
      <div>
        <ButtonMixed txt="button" />
        <LabelMixed txt="label" />
      </div>
    )
  }
}

export default Mixins;
```
