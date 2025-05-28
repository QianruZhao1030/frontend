# Vue底层实现原理

- vue.js采用数据劫持+发布订阅模式

- Observe数据监听

  - 通过Object.defineProperty()监听数据变化，它内部可以定义getter和setter。

  - 数据变化，触发setter。

  - Observer通知Watcher

  <img src="https://api2.mubu.com/v3/document_image/28886397_5a3d967a-4206-42fd-c488-1d54ce5a4295.png" alt="img" style="zoom:25%;" />

- Watcher订阅者

  - Observe和Compile的桥梁

  - 实例化时往属性订阅器dep中添加自己

  - 有update()

  - 属性变动，dep.notice()通知，调用update()，触发Compile回调

- Compile指令解析器

  - 解析模版指令，将变量替换成数据渲染页面。

  - 每个指令对应的节点绑定更新函数，添加Watcher，数据变化更新视图

# Vue响应式原理

- vue2 使用Object.defineProperty 劫持对象属性，当属性发生变化时，触发对应的回调函数。但是不能监听数组的变化，需要使用重写数组的方法来监听数组的变化。还有不能监听对象的添加和删除。嵌套数组和对象需要深度遍历。

  > [!NOTE]
  >
  > 数据劫持：把data中数据改成getter,setter形式，实现响应式。
  > 数据代理：把_data中的数据放到vm中一份，实际用的是Object.defineProperty
  > 数组中的项没有getter，setter
  > 重写数组：原型链方法+重新解析模版生成虚拟dom等流程触发试图更新。push,pop,shift,unshift,splice,sort,reverse

- vue3 使用Proxy 劫持对象，当对象的属性发生变化时，触发对应的回调函数。

- 关闭响应式<img src="https://api2.mubu.com/v3/document_image/28886397_914be960-9ced-4dd8-90e7-f366690cdeb0.png" alt="img" style="zoom: 33%;" />
  markRaw()标记对象为非响应式；toRaw()返回由 reactive 或 ref 创建的响应式对象的原始对象；shallowReactive 仅对对象的顶层属性创建响应式，shallowRef：仅对 .value 的赋值操作创建响应式

# Vue2和3区别

**响应式原理**

​	2：Object.defineProperty劫持对象属性，无法检测新增/删除属性，需要$set/$delete（不能配data中一级数据，即根数据对象）。

​	3：proxy代理。不需要遍历，会自动监听所有属性，有利于性能的提升。支持更多数据类型的响应式追踪（如Map/Set等）

**组合式api**

- vue2 生命周期钩子使用选项式API，将数据和函数集中起来处理（data/methods等选项组织代码）

- vue3 新增组合式API（setup + 响应式API生命周期名称前加 on），将同一个功能的代码集中起来处理支持更好的逻辑复用和代码组织

**性能优化**

- vue3 虚拟DOM算法优化（编译器生成带更新标记的虚拟DOM）

- vue3 打包体积更小（更好的tree-shaking支持）

- vue3 渲染速度提升（静态节点提升、事件缓存等）

**生命周期**
	创建前：beforeCreate -> 使用setup()
	创建后：created -> **使用setup()新增**
	挂载前：beforeMount -> onBeforeMount
	挂载后：mounted -> onMounted
	更新前：beforeUpdate -> onBeforeUpdate
	更新后：updated -> onUpdated
	**销毁前：beforeDestroy -> onBeforeUnmount**
	**销毁后：destroyed -> onUnmounted**
	异常捕获：errorCaptured -> onErrorCaptured
	被激活：onActivated 被包含在<keep-alive>中的组件，会多出两个生命周期钩子函数。被激活时执行。
	切换：onDeactivated 比如从 A 组件，切换到 B 组件，A 组件消失时执行

**根节点**：2单根；3没有要求，默认会加fragement。减少内存

**全局API**

- vue2 全局API挂载Vue对象（Vue.use/Vue.component）

- vue3 改为应用实例API（createApp().use()）

**TypeScript支持**

- vue3 使用TypeScript重写，提供更好的类型推导

- vue3 组件选项支持类型声明（defineComponent）

**v-if /v-for优先级**

- 2v-for优先级高，v-if会分别运行在循环中。 若遍历数组大，真正展示的少，会有性能浪费。
- 3v-if高，一起使用报错。由于语法歧义，建议先使用computed过滤数据。

**diff**

- 2：遍历每一个虚拟节点，进行虚拟节点对比，并返回一个patch对象，用来存储两个节点不同的地方。 用patch记录的消息去更新dom。

- 3：给每一个虚拟节点添加一个patchFlags。只会比较patchFlags发生变化的节点，进行识图更新。



# vue3好处（******）

- 重写了虚拟 Dom 实现，编译模板的优化，更高效的组件初始化

- 更小的打包体积，减少了前端加载时间。

- 采用 TypeScript 重写，提供了更好的类型推断和类型提示。

- 灵活api

- 更好的响应系统：proxy

# Vue生命周期

- beforeCreate

- created

  - data有值，未挂载

  - vue实例被创建

- beforeMount
  - 可发请求，取数据

- mounted
  - 操作dom

- beforeUpdate
  - vue实例data变化，触发组建重新渲染

- updated

- beforeDestory
  - 可手动销毁

- destoryed

- 父子组件：父beforeCreated,父created,父beforeMounted,子beforeCreated,子created，子beforeMount，子mounted，父mounted，父beforeUpdated，子beforeDestory，子destoryed，父updated

# vue虚拟DOM

虚拟DOM实际上一个javaScript对象，用来表示真实DOM的数据结构。但是不会直接与浏览器交互，虚拟DOM的作用主要目的是减少直接操作真实DOM的次数，从而提高性能。

- 工作原理
  - 创建虚拟DOM：当一开始vue组件渲染的时候，Vue会创建一个虚拟DOM树，表示组件的结构个状态
  - 更新虚拟DOM：当组件状态发生变化的时候，Vue会重新生成一个新的虚拟DOM树
  - 比较差异：Vue使用一种差异算法，来比较新旧虚拟DOM树之间的差异。
  - 更新真实DOM：找到差异，计算出最小的DOM操作，并将这些操作应用到真实DOM上

# Vue diff

当组件创建和更新时，vue均会执行内部的update函数，该函数使用render函数生成的虚拟dom树，将新旧两树进行对比，找到差异点，最终更新到真实dom

对比差异的过程叫diff，vue在内部通过一个叫patch的函数完成该过程

在对比时，vue采用深度优先、同层比较的方式进行比对。

在判断两个节点是否相同时，vue是通过虚拟节点的key和tag来进行判断的

具体来说，首先对根节点进行对比，如果相同则将旧节点关联的真实dom的引用挂到新节点上，然后根据需要更新属性到真实dom，然后再对比其子节点数组;如果不相同，则按照新节点的信息递归创建所有真实dom，同时挂到对应虚拟节点上，然后移除掉旧的dom。

在对比其子节点数组时，vue对每个子节点数组使用了两个指针，分别指向头尾，然后不断向中间靠拢来进行对比，这样做的目的是尽量复用真实dom，尽量少的销毁和创建真实dom。如果发现相同，则进入和根节点一样的对比流程，如果发现不同，则移动真实dom到合适的位置。这样一直递归的遍历下去，直到整棵树完成对比。

1. diff的时机 (_update)

当组件创建时，以及依赖的属性或数据变化时，会运行一个函数，该函数会做两件事:

- 运行_render生成一棵新的虚拟dom树(vnode tree)

- 运行_update，传入虚拟dom树的根节点，对新旧两棵树进行对比，最终完成对真实dom的更新

```javascript
// vue构造函数
function vue(){
  //...其他代码
	var updatecomponent =()=>{this._update(this._render())}
	new Watcher(updateComponent);
  //其他代码
}
```

2. __update 函数在干什么
   _update函数接收到一个vnode 参数，这就是新生成的虚拟dom树。

   同时，_update函数通过当前组件的_vnode属性，拿到旧的虚拟dom树。

   update函数首先会给组件的vnode 属性重新赋值，让它指向新树

   <img src="/Users/burst/Library/Application Support/typora-user-images/image-20250515142437428.png" alt="image-20250515142437428" style="zoom:33%;" />

   然后会判断旧树是否存在:
   	不存在:说明这是第一次加载组件，于是通过内部的patch函数，直接遍历新树，为每个节点生成真实DOM，挂载到每个节点的 elm属性上

   <img src="/Users/burst/Library/Application Support/typora-user-images/image-20250515142522839.png" alt="image-20250515142522839" style="zoom:25%;" />

   ​	存在:说明之前已经渲染过该组件，于是通过内部的patch函数，对新旧两棵树进行对比，以达到下面两个目标:
   ​		完成对所有真实dom的最小化处理
   ​		让新树的节点对应合适的真实dom

   <img src="/Users/burst/Library/Application Support/typora-user-images/image-20250515142643885.png" alt="image-20250515142643885" style="zoom:25%;" />

3. patch函数的对比流程
   术语解释:
   1.「相同」:是指两个虚拟节点的标签类型、key值均相同，但input元素还要看type属性

   2.「新建元素」:是指根据一个虚拟节点提供的信息，创建一个真实dom元素，同时挂载到虚拟节点的elm属性上
   3.「 销毁元素 」:是指:vnode.elm.remove()
   4.「更新」:是指对两个虚拟节点进行对比更新，它仅发生在两个虚拟节点「相同」的情况下。具体过程稍后描述。
   5.「对比子节点」:是指对两个虚拟节点的子节点进行对比，具体过程稍后描述

   详细流程:
   **1.根节点比较**

   <img src="/Users/burst/Library/Application Support/typora-user-images/image-20250515142905683.png" alt="image-20250515142905683" style="zoom:25%;" />

   patch函数首先对根节点进行比较如果两个节点:
   「相同」，进入「更新」流程
   1，将旧节点的真实dom赋值到新节点:newnode.elm= oldvnode.elm

   2.对比新节点和旧节点的属性，有变化的更新到真实dom中

   3.当前两个节点处理完毕，开始「对比子节点」

   不「相同」
   1.新节点递归「新建元素」
   2.旧节点「销毁元素」

   **2.对比子节点**
   在「对比子节点」时，vue-切的出发点，都是为了:
   尽量啥也别做
   。不行的话，尽量仅改动元素属性
   。还不行的话，尽量移动元素，而不是删除和创建元素
   还不行的话，删除和创建元素

### **Vue2 双端Diff算法**

1. **遍历方式**：采用双端比较（头头、尾尾、头尾、尾头）
2. **节点复用**：通过4个指针交叉比较旧新子节点数组
3. **移动策略**：优先处理相同节点，最后处理新增/删除节点
4. **时间复杂度**：O(n) 但存在较多冗余比较

### **Vue3 快速Diff算法**

1. 预处理阶段
   - 前序相同节点直接复用
   - 后序相同节点直接复用
2. 核心Diff
   - 构建key-index映射表（keyed fragments）
   - 寻找最长递增子序列（LIS）作为稳定锚点
3. 移动策略
   - 仅处理非稳定序列节点
   - 最小化DOM移动操作
4. **时间复杂度**：O(n) + O(k)（k为最长递增子序列长度）

**关键差异对比**

| 特性                                                      | Vue2                | Vue3                   |
| --------------------------------------------------------- | ------------------- | ---------------------- |
| 算法类型                                                  | 双端比较            | 快速Diff + LIS优化     |
| key的作用                                                 | 辅助节点匹配        | 关键索引依据           |
| 移动优化                                                  | 简单位置交换        | 最小化DOM操作          |
| 静态节点处理                                              | 全量比较            | 静态提升跳过比较       |
| 动态列表性能                                              | 平均O(n)            | 接近O(1)稳定序列场景   |
| 内存占用                                                  | 较高（维护4个指针） | 较低（使用位运算标记） |
| vue2 使用双端比较算法，先比较头尾节点，然后比较剩余节点。 |                     |                        |

# computed & watch

- 监听

  - 都可实现监听

  - computed依赖值改变，计算属性也会改变

  - watch监听data变量，触发watch中的方法

- watch  

  - 对象：键监听属性，值回调函数

  - 一条数据影响多个

- computed

  - 值会被缓存，无改变会从缓存读取值

  - 必须returm结果

  - 多个数据影响一个

| **特性**     | **computed**（计算属性）                | **watch**（监听器）                                      | **methods**（方法）              |
| ------------ | --------------------------------------- | -------------------------------------------------------- | -------------------------------- |
| **调用方式** | 像属性一样访问（`this.fullName`）       | 监听特定数据变化触发回调                                 | 主动调用（`this.handleClick()`） |
| **缓存机制** | 依赖不变时自动缓存结果                  | 无缓存，每次变化都执行回调                               | 无缓存，每次调用都执行           |
| **适用场景** | 基于已有数据计算新值（如格式化、筛选）  | 数据变化后执行异步操作或复杂逻辑                         | 事件处理、需要副作用的操作       |
| **异步操作** | ❌                                       | ✅                                                        | ✅                                |
| **代码形式** | 声明式（返回计算结果）<br />get(),set() | 命令式（监听函数）<br />参数：handler()，deep，immediate | 命令式（函数体）                 |

# data为什么是函数

- 组件被复用就会创建多个实例，实际都是一个构造函数

- 若data是对象，作为引用类型，一个改变会影响其它

- 为了保证组件实例的data之间不冲突，data得是函数

# key作用

- 当列表中的元素被添加、删除、重新排序时，框架需要判断哪些元素发生了变化。 key框架可以快速定位到对应的元素，避免全量比较。

- 当元素被移动或重新排序时，`key` 可以帮助框架保留元素的状态（输入值、动画进度）

- 如果没有 `key`，框架默认按元素位置（索引）比较，可能导致错误复用。（eg在列表头部插入元素时，索引变化会导致所有后续元素重新渲染）

- `key` 的核心作用是**唯一标识同级元素**，帮助算法快速识别元素的变化类型（新增、删除、移动、更新），从而避免不必要的 DOM 操作，提升渲染效率。


**不能是index？**

1.若对数据进行:逆序添加、逆序删除等破坏顺序操作:会产生没有必要的真实DOM更新 ==>界面效果没问题，但效率低
2.如果结构中还包含输入类的DOM:会产生错误DOM更新 ==>界面有问题

| 特性                | React                     | Vue                        |
| ------------------- | ------------------------- | -------------------------- |
| **强制要求**        | 必须为列表项提供 `key`    | 非强制，但强烈推荐         |
| **推荐 `key` 类型** | 稳定 ID（如数据唯一标识） | 稳定 ID（如数据唯一标识）  |
| **索引作为 `key`**  | 不推荐，可能导致状态异常  | 允许但不推荐，性能较差     |
| **其他场景**        | 仅用于列表                | 还用于条件渲染、动态组件等 |

# 组件通信

- 父子

  - props，emit
    1、父组件绑定自定义事件@/v-on，子组件触发事件this.$emit('fushijian',  ***)
    2、父组件中子组件先绑定ref=aaa，mounted时可以this.$ref.aaa.$on('shijian', 箭头函数)，子组件触发事件this.$emit('fushijian',  数据)

- 全局组件通信（父子、兄弟、跨级）Event Bus
  1、安装全局事件总线new Vue({... ,beforeCreate(){Vue.prototype.$bus = this},...})
  2、接受数据组件，this.$bus.on('shijian',箭头函数)
  3、发送数据组件，this.$bus.$emit('fushijian', 数据)

- vuex

  - 多级组件嵌套传递、变更数据

- $attrs/$listeners

  - 多级组件嵌套传递数据
    - 两个对象 父：<child-com1 :foo="foo" :boo="boo" :coo="coo" :doo="doo" title="前端工匠"></child-com1> 子 ：$attrs 里存放的是父组件中绑定的非 Props 属性 props: {    foo: String // foo作为props属性绑定  },  created() {    console.log(this.$attrs); // { "boo": "Html", "coo": "CSS", "doo": "Vue", "title": "前端工匠" }  }

- provide/inject

  - 非响应模式provide变了，inject值不会变 

    ```
    // A.vue
    export default {  provide: {    name: '浪里行舟'  }}/
    / B.vue
    export default {  inject: ['name'],  mounted () {    console.log([this.name](http://this.name/));  // 浪里行舟  }}
    ```

  - 响应 

    ```
    export default {  provide: {    theme: this  }}或provide() {  
    this.theme = Vue.observable({color: "blue"});  
    return {    theme: this.theme  };}
    inject: {    theme: {      //函数式组件取值不一样      default: () => ({})    }  }
    ```

    

# vuex

- 2只能用3版本，3用4版本

- why（共享）
  - 多个组件依赖于同一状态 不同组件的行为需要变更同一状态

- 状态管理模式，核心是store

- 存储状态时响应式

  - store中状态变化，相应组件会更新

  - 变更状态唯一方式就是mutation

- 核心模块

  - state：定义数据

  - Getter：同计算属性，返回值会根据依赖存储
    store.getters.addcount

  - action：Action 提交的是 mutation，不是直接变更状态。一般会有异步函数

  - mutation：唯一更改store中状态方式，必须是同步函数

  - moudule：允许将单一的store拆分未多个，且保存在统一状态树中

# vue-router

用于实现单页面应用（SPA）的路由功能

**路由模式**

- **hash 模式**（默认）：URL 带 `#` 符号（如 `http://example.com/#/home`），兼容性好。

  -  **核心机制**
     - **监听 `hashchange` 事件**：当 URL 的 hash 值（`#` 后的部分）变化时，触发事件并更新视图，不触发浏览器重新加载。
     - **修改 hash**：通过 `window.location.hash = '/new-path'` 改变 URL，浏览器会记录历史，但不向服务器发送请求。

- **history 模式**：使用 HTML5 History API，URL 更美观（如 `http://example.com/home`），需服务器配置支持。

  - 核心机制

    - HTML5 History API：通过pushState和replaceState

      方法操作浏览器历史记录，改变 URL 但不触发页面刷新。

      - `history.pushState(state, title, path)`：添加新的历史记录。
      - `history.replaceState(state, title, path)`：替换当前历史记录。

    - **监听 `popstate` 事件**：当用户点击浏览器后退 / 前进按钮时触发，更新视图。

**导航模式**

- **声明式导航**：使用 `<router-link to="/home">Home</router-link>`组件。
- **编程式导航**：使用 `router.push('/home')`or`router.push({ name: 'User', params: { id: 123 } });`，`router.replace`

**动态路由参数**

```
{ path: '/user/:id', component: User } // 路由配置
this.$route.params.id; // 访问动态参数
```

**导航守卫**：登录验证，权限控制

```
router.beforeEach((to, from, next) => {
  if (to.meta.requiresAuth && !isAuthenticated()) {
    next('/login'); // 未登录时重定向到登录页
  } else {
    next(); // 允许访问
  }
});
```

**其他**

```javascript
{
  path: '/about',
  component: () => import('./views/About.vue') // 路由懒加载，使用动态 import
  meta: { requiresAdmin: true } // 自定义元信息
}
```

# nextTick

**DOM 更新后执行回调函数**

- why？

  - DOM更新是异步执行的，修改响应式数据时，会将任务放在更新队列中，抽空执行。因此你在修改后立即访问DOM会得到更新前数据。

- Vue的nextTick实现主要基于JavaScript事件循环机制，精准控制执行顺序，事件循环是唯一能实现 “异步等待” 的底层机制，通过将回调注册到任务队列中，让引擎在合适的时机自动执行。

  ### 关键实现机制

  1. **微任务优先**：加入任务队列

  - 优先使用Promise.then()（现代浏览器）（**UI 渲染之前**）
  - 回退方案：MutationObserver → setImmediate → setTimeout（**UI 渲染之后**执行）

  2. **异步更新队列**

  ```
  const callbacks = [] // 回调队列
  let pending = false // 批量处理标志
  
  function flushCallbacks() {
    pending = false
    const copies = callbacks.slice(0)
    callbacks.length = 0
    for (let i = 0; i < copies.length; i++) {
      copies[i]()
    }
  }
  ```

  1. **执行优先级**

  - 数据变化 → 触发Watcher → 将更新推入队列
  - 同一事件循环内的数据变化会被批量处理
  - DOM更新完成后执行nextTick回调

  ### 核心特点

  - **批处理优化**：同一tick内的多次nextTick调用会合并执行
  - **环境适配**：自动选择最优的微任务实现方式
  - **错误处理**：在微任务中捕获异常并通过console.error输出

  ### 使用示例

  ```
  // Promise风格
  this.$nextTick().then(() => {
    // DOM更新后执行
  })
  
  // 传统回调风格
  this.$nextTick(() => {
    // 可访问更新后的DOM
  })
  ```


# keep-alive

- 在组件切换时，对被移除的组件实例进行缓存

- 功能：1、组件缓存，保持组建状态。2、减少性能消耗，避免重复渲染造成性能问题。3、保留组件状态，eg表单内容、滚动条

- 三个属性：include，exclude，max

- 渲染机制：vue.is是将Dom抽象成VNode。keep-alive实际是缓存VNode组件在cache中。重新渲染时将VNode从cache中取出。

- 生命周期：activated：组件被激活时调用（组件缓存后不会触发created，mounted）。deactivated：组件被停用时调用

- 场景：tabs标签页；在单页应用（SPA）中缓存路由组件，防止用户返回时页面状态丢失

内存溢出：

- 未设置max，大组件缓存，动态组件滥用

清除： `$parent.$options.cache.delete(key)` ，deactivated清理定时器、websocket等

# 插槽

**默认插槽**：子组件定义插槽位置，父组件插入内容

子`<slot>默认内容（父组件未传值时显示）</slot>`

父`<MyComponent>  <p>自定义内容</p></MyComponent>`

**具名插槽**：子组件定义多个插槽位置，父组件通过名称区分

子`<slot name="header">默认标题</slot>`

父 `<template #header> <h1>自定义标题</h1></template>`

**动态插槽**

父

```html
<template #[name]> <h1>自定义标题</h1></template>
const name = ref('header')
```

**作用域插槽**：子组件向父组件暴露内部数据，父组件自定义渲染逻辑

​	子组件通过 `<slot :item="item">` 暴露数据，父组件通过 `v-slot="slotProps"` (slotProps.item.name)或解构直接取 `v-slot="{ item }"` 接收

​	子组件决定**渲染位置**，父组件决定**渲染内容**。

子

```html
<slot name="item" v-for="item in items" :item="item">
    {{ item.name }} <!-- 默认渲染方式 -->
</slot>
```

父

```html
<List>
  <template #item="{ item }">
    <li>{{ item.name }} ({{ item.age }})</li>
  </template>
</List>
```
