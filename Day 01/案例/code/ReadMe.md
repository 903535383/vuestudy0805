# Vue.js  Day01
+ Vue.js的引入方式
```html
    <!-- 1. 外引方式 通过 使用Url的方式 -->
    <script src="https://cdn.jsdelivr.net/npm/vue@2.6.10/dist/vue.js"></script>
    <!-- 2. 本地文件的方式引入 -->
    <script src="./lib/vue.js"></script>
```
## Vue.js  代码结构

```js
    // 2. 创建Vue 实例对象
        var vm = new Vue({
            el:'#app',  //选择器的名称 表示new的实例,要控制页面上的哪一个区域
            data:{   //data就是存放el中要用到的数据
            msg:'欢迎学习Vue'  //指令

            }
        }) 
```

### v-cloak指令的学习
> 案例
```html
<div id="app">
        <!-- 1. 插值{{}} 会应为加载顺序的问题造成闪烁 通过使用v-cloak 来解决 -->
        <h3 v-cloak>{{msg}}</h3>
        <!-- 2. 使用v-text也可以解决闪b烁问题 -->
        <h2 v-text="msg"></h2>

        <!-- 插值{{}}表达式和v-text的区别 -->
        <p>++++++++{{ msg }}++++++++++</p>
        <p v-text="msg">===============</p>
        <!-- v-text默认没有闪烁问题,v-text会覆盖元素中原本的位置
        但是插值表达式只会替换自己的展位符,不会把整个元素的内容替换 -->

    </div>
```


#### `v-text` 和 `v-html`


#### `v-bind`指令

1\. 在vue中,v-bind的是用来绑定属性的指令
使用 **v-bind** 有3中方式
+ 直接使用v-bind指令
+ 使用简化指令
+ 拼接绑定内容


#### `v-on`指令
> Vue中提供`v-on`时间绑定机制
