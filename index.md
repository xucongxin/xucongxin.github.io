## React组件生命周期

React组件的生命周期一般来说是分为两个部分的，第一部分是初次渲染，第二部分是状态更新导致的再次渲染。在这里我们只说Class组件，不说fun组件

### 首次渲染

一般来说一个class组件里面有如下方法，react组件首次渲染经历了如下过程。


```markdown
// 定义一个TodoList的React组件，通过继承React.Component来实现
class TodoList extends React.Component {
  ...
}
```
# 构造函数constructor
在生命周期开始的时候，调用构造函数进行初始化工作，在创建组件的时候只调用一次。
```markdown
constructor(props) {
   //绑定this
    super(props);
    //设置初始状态
    this.state = {
    date: new Date()
    };
    //为函数绑定this
    this.handleChange = this.handleChange.bind(this);
  }

```

