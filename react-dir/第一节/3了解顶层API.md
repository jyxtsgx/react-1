## 3. `了解顶层API`

### `react.js`
```
React.Children: Object
React.Component: ReactComponent(props, context, updater)
React.DOM: Object
React.PropTypes: Object
React.cloneElement: (element, props, children)
React.createClass: (spec)
React.createElement: (type, props, children)
React.createFactory: (type)
React.createMixin: (mixin)
React.isValidElement: (object)
```


`Component API`
```
this.context: Object
this.props: Object
this.refs: Object
this.state: Object
this.setState: Object
```
### `react-dom.js`

```
ReactDOM.findDOMNode: findDOMNode(componentOrElement)
ReactDOM.render: ()
ReactDOM.unmountComponentAtNode: (container)
```

### `react-dom-server.js`

```
ReactDOMServer.renderToString
ReactDOMServer.renderToStaticMarkup
```
