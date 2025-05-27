**CDN**

[https://unpkg.com/vue](https://unpkg.com/vue)

[https://cdn.jsdelivr.net/npm/vue/dist/vue.js](https://cdn.jsdelivr.net/npm/vue/dist/vue.js)

  

  

<script src="https://unpkg.com/vue@3/dist/vue.global.js"></script>

<script type="module">   
import { createApp } from 'https://unpkg.com/vue@3/dist/vue.esm-browser.js'  

</script>

  

npm init vue@3

npm init [vue@2](mailto:vue@2)  
  
Option api

Composition

Ref api

  

  

**搭建脚手架**

npm install vue-cli -g

vue -V

npm install @vue/cli -g  (3.0版本)

npm uninstall vue-cli -g  
$ vue create antd-demo  

  

Vite

$ yarn create vite  

$ npm create vite@latest  

  

----------------- **vue3** --------------

> npm init [vue@latest](mailto:vue@latest)  

  

npm init @vitejs/app

npm install vue-router@next [vuex@next](mailto:vuex@next)

  

const { proxy } = getCurrentInstance() as ComponentInternalInstance;

内置组件

我们常常会将 `<Suspense>` 和 [`<Transition>`](https://cn.vuejs.org/guide/built-ins/transition.html)、[`<KeepAlive>`](https://cn.vuejs.org/guide/built-ins/keep-alive.html) 等组件结合。要保证这些组件都能正常工作，嵌套的顺序非常重要。

另外，这些组件都通常与 [Vue Router](https://router.vuejs.org/zh/) 中的 `<RouterView>` 组件结合使用

  

  

defineComponent(props, setup() => return )  

defineProps(['title'])

defineEmits(['update:modelValue])

Proxy

Reflect

interface.  类型

ref //string, number, boolean, array(value响应式对象)

toRefs(obj, key)  //toRef(obj, 'age')

//ref是对原始数据的拷贝，当修改ref数据时，模板中的视图会发生改变，但是原始数据并不会改变。 toRef是对原始数据的引用，修改toRef数据时，原始数据也会发生改变，但是视图并不会更新。

Ref 

reactive //obj

响应式顺序：effect > track > trigger > effect  

在组件渲染过程中，一个 effect 会会触发get，从而对值进行 track，当值发生改变，就会进行 trigger，执行 effect 来完成一个响应.  

computed

onmount

onUnmount

  

class funcName

      constructor(){}

new funcName

  

export const useUserStore = defineStore('user', () => {}）

  

  

  

  

  

  

-----------------  **Vue2**  ------------

# [Vue 2 技术栈归纳与精粹](https://uinika.github.io/Web/Vue/)

**常用语法**

v-bind:title = "message" 缩写 :title = "message:

v-if="seen"

v-for="todo in todos"

v-on:click="reverseMessage" 缩写 @click="reverseMessage"

v-once

v-html

v-model 表单输入绑定

[.lazy](https://cn.vuejs.org/v2/guide/forms.html#lazy)

[.number](https://cn.vuejs.org/v2/guide/forms.html#number)

[.trim](https://cn.vuejs.org/v2/guide/forms.html#trim)

v-if="loginType"

v-else-if="type"

v-else

v-show 不支持 <template> 元素，也不支持 v-else

v-for 的优先级比 v-if 更高

is="todo-item"

  

修饰符  

.native (@focus.native="onFocus")

.sync (:title.sync="doc.title")

v-on 

- .stop
- .prevent
- .capture
- .self
- .once
- .passive

  

v-on:submit.prevent="onSubmit"

v-on:scroll.passive="onScroll"

v-on:keyup.enter="submit"

v-on:keyup.13="submit"

- .enter
- .tab
- .delete 
- .esc
- .space
- .up
- .down
- .left
- .right

Vue.config.keyCodes.f1 = 112

- .ctrl
- .alt
- .shift
- .meta

@keyup.alt.67="clear"

@click.ctrl.exact="onCtrlClick"

  

methods

computed 计算属性

  

**component**

<my-component v-for="(item, index) in items" v-bind:item="item" :index="index" :key="key"></my-component>

<custom-input v-model="searchText" ></custom-input>

Vue.component('custom-input', {

props: ['value'],

template:'<input v-bind:value= "value" v-on:input="$emit('input', $event.target.value)">'

})

  

$event.target.value

$event 原始dom或数据

vm.data

$attrs $listeners

$emit 方法 调用父组件方法

$emit('change', $event.target.checked)

vm.$emit('input', event.target.value)

  

<child2 v-bind="$attrs" v-on="$listeners"></child2>  

##### Vue中 常见的组件通信方式可分为三类 

- 父子通信 : 父向子传递数据是通过 props，子向父是通过 events（$emit）； 通过父链 / 子链也可以通信（$parent / $children）； ref 也可以访问组件实例； provide / inject； $attrs/$listeners；

- 兄弟通信 : Bus； Vuex；  
    

- 跨级通信 : Bus； Vuex； provide / inject、 $attrs / $listeners、  
    

$attrs–继承所有的父组件属性（除了 prop 传递的属性、class 和 style ），一般用在子组件的子元素上

listeners属性，它是一个对象，里面包含了作用在这个组件上的所有监听器，你就可以配合v−on=”listeners” 将所有的事件监听器指向这个组件的某个特定的子元素。（相当于子组件继承父组件的事件）

  

  

<text-document v-bind:title="doc.title" v-on:update:title="doc.title = $event" ></text-document>

this.$emit('update:title', newTitle)

  

  

  

**vue工具插件**  

**【Vuex】**

Vue.use(Vuex)

State

this.$store.state

mapState

getters

mapGetters

Mutation 更新state

  

**【VueRouter】**

Vue.use(VueRouter)

<router-link to="/foo">

<router-link :to="{ name: 'account-settings-base' }">基本设置</router-link>  

<router-view>

this.$router.params

this.$router

this.$route

$route.meta.title  

this.$store.dispatch

const {

        $route: {

          query: { id }

        }

      } = this

<router-link

                to={{

                  name: 'dec_export_check_declare_info',

                  query: {

                    id: record.id

                  }

                }}

              >

</router-link>

  

【plugins】

[wangeditor](https://www.wangeditor.com/)  

  

【npm SSR、Express】

npm install vue vue-server-renderer --save

npm install express --save

  

**Antd**

import Tooltip from 'ant-design-vue/es/tooltip'

  

  

**VueComponents**

v-viewer

vue-lazyload

[vue-json-excel](https://github.com/jecovier/vue-json-excel)  

v-calendar

vue-pdf

vue-cropper

vue-contextmenu

vue-clipboard2

  

  

**vue源码分析**

```
vm.$vnode
vm.$slots
vm.$scopedSlots响应式机制的主要功能就是，可以把普通的 JavaScript 对象封装成为响应式对象，拦截数据的获取和修改操作，实现依赖数据的自动化更新。相比于 Vue2 使用的 Object.defineProperty，Vue3 不需要提前递归收集依赖，初始化的速度更快；
Vue2 收集依赖的过程中会产生很多的 Dep 对象，Vue3 可以节省这部分的内存开销；
Vue2 无法监听数组、对象的动态添加、删除，需要通过 $set、$delete，增加学习成本；
Vue2 无法监听 Set、Map，只能处理普通对象。
```

# `React 和 Vue 框架的区别`

`其实react和vue大体上是相同的，   比如都使用虚拟DOM高效的更新视图，   都提倡组件化，   都实现了数据驱动视图，   都使用diff算法，   也都对diff算法进行了优化，   都有router库实现url到组件的映射，   都有状态管理等等   `  

`**vue 样式穿透scss/sass**`

`**<style  lang="scss" scoped>   **`

`**Sass 之类的预处理器无法正确解析 >>>。这种情况下你可以使用 /deep/ 或 ::v-deep 操作符取而代之   **`

`**父选择器&   **`

`**子选择器>   **`

**其他**

**:class="{ 'popup-height': type === 'left' || type === 'right' }"  
**