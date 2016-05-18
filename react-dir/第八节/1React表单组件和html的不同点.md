## 1. `React表单组件和 html 的不同点`

- `value/checked` 属性设置后，用户输入无效
- `textarea` 的值要设置在 `value` 属性

```
<textarea name="description" value="This is a description." />
```

- `select` 的 `value` 属性可以是数组，不建议使用 `option` 的 `selected` 属性

```
<select multiple={true} value={['B', 'C']}>
   <option value="A">Apple</option>
   <option value="B">Banana</option>
   <option value="C">Cranberry</option>
 </select>
```


- `input/textarea` 的 `onChange` 用户每次输入都会触发（即使不失去焦点）
- `radio/checkbox/option` 点击后触发 `onChange`
