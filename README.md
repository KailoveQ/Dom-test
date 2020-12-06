# Dom-test
预览链接
## 课后作业
## [预览链接](https://kailoveq.github.io/Dom-test/dist/index.html)
## 代码
```js
window.dom = {

    // ***************************************** 
    find(selector, scope) {
        return (scope || document).querySelectorAll(selector)
    },
    // ***************************************** 
    style(node, name, value) {
        if (arguments.length === 3) {
            //dom.style(div,'color','red')
            node.style[name] = value
        } else if (arguments.length === 2) {
            if (typeof name === 'string') {
                //dom.style(div,'color')
                return node.style[name]
            } else if (name instanceof Object) {
                //dom.style(div,{color:'red'})
                const object = name
                for (let key in object) {
                    node.style[key] = object[key]
                }
            }
        }
    },
    // ***************************************** 
    each(nodeList, fn) {
        for (let i = 0; i < nodeList.length; i++){
            fn.call(null,nodeList[i])
        }
    }


}
```
