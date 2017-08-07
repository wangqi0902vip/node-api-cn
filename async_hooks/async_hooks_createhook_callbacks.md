
<!-- YAML
added: v8.1.0
-->

* `callbacks` {Object} the callbacks to register
* Returns: `{AsyncHook}` instance used for disabling and enabling hooks

对于每一个异步操作的不同生命周期都会调用注册的回调方法。

在生命周期中会调用各自异步事件的 `init()`/`before()`/`after()`/`destroy()`回调方法。

所有的回调方法都是可选的。所以，比如说，如果只有资源清理操作需要跟踪，那么只要传递`destroy`就行了。 
回调方法的具体细节会在后面的章节[`Hook Callbacks`][]体现.

