### VNode


虚拟节点数据结构：

```js
var VNode = function VNode (
  tag,
  data,
  children,
  text,
  elm,
  context,
  componentOptions,
  asyncFactory
) {

  this.tag = tag;							// 标签
  this.data = data;							// 数据
  this.children = children;					// 子孙节点
  this.text = text;							// 文本
  this.elm = elm;							// 元素
  this.ns = undefined;						// 命名空间
  this.context = context;
  this.fnContext = undefined;
  this.fnOptions = undefined;
  this.fnScopeId = undefined;
  this.key = data && data.key;
  this.componentOptions = componentOptions;
  this.componentInstance = undefined;
  this.parent = undefined;					// 父节点
  this.raw = false;
  this.isStatic = false;
  this.isRootInsert = true;
  this.isComment = false;
  this.isCloned = false;					// 是否克隆
  this.isOnce = false;
  this.asyncFactory = asyncFactory;			// 异步工厂
  this.asyncMeta = undefined;
  this.isAsyncPlaceholder = false;
};

```


节点操作方法：
```js
var nodeOps = Object.freeze({

	createElement: createElement$1,
	createElementNS: createElementNS,
	createTextNode: createTextNode,
	createComment: createComment,
	insertBefore: insertBefore,
	removeChild: removeChild,
	appendChild: appendChild,
	parentNode: parentNode,
	nextSibling: nextSibling,
	tagName: tagName,
	setTextContent: setTextContent,
	setStyleScope: setStyleScope
	
});
```