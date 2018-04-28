#### strats

合并策略

```js
propsData
el
data
beforeCreate
created
beforeMount
mounted
beforeUpdate
updated
beforeDestroy
destroyed
activated
deactivated
errorCaptured
components
directives
filters
watch
computed
inject
methods
props
provide
```

默认合并策略

```js
var defaultStrat = function (parentVal, childVal) {
  return childVal === undefined
    ? parentVal
    : childVal
};
```