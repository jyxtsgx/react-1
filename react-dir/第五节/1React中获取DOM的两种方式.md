## 1. `React 中获取DOM的两种方式`
- ReactDOM.findDOMNode
- this.refs.xxx

获取DOM后可以方便结合现有非 react 类库的使用，通过 ref/refs 可以取得组件实例，进而取得原生节点，不过尽量通过 state/props 更新组件，不要使用该功能去更新组件的DOM。
