# frontend
# 自我介绍

面试官您好，我是赵倩茹，非常荣幸能来参加此次面试。我毕业于杭州电子科技大学计算机技术专业。在前端开发领域，我积累了较为丰富的工作经验。2021 年 7 月 - 2025 年 2 月期间，我就职于北京转转精神科技有限公司担任前端工程师，主要负责公司支付和财务方向的项目。

## 收单路由

旨在打造一个能支持多种支付通道的配置化支付路由系统，满足用户多样化支付场景需求。

1. 项目过程中，最大的难点在于如何实现多种支付方式、终端、资金池和业务场景之间复杂的联动关系。我负责搭建基于 React + Ant Design 的路由系统，开发复杂联动表单。为了解决这个难题，我深入研究各个组件之间的数据流向和交互逻辑，将整体功能拆解成一个个小模块，逐一攻克。最终成功实现了预期的复杂联动效果，提升了系统的稳定性和用户体验。
2. 面对复杂技术挑战时，能够提出高效且风险最小的解决方案。eg：在收单路由项目中，面对接口数据结构的大幅变更和收银台逻辑的复杂性。我通过精准改造接口数据层，有效降低了代码迁移成本，同时实现了代码解耦，确保了系统的稳定性和可维护性。

## 收银台接入支付渠道

随着业务快速发展，收银台需要接入多种支付渠道。项目涉及 H5 收银台、转转小程序等多个终端，同时需要与客户端、小程序及第三方支付渠道进行深度交互。

1. 独立负责h5收银台、转转小程序接入新的支付渠道，如微企付、京东支付等，确保收银台能吊起支付渠道。
2. 设计并实现可动态配置的小程序支付方式接入架构，实现"即插即用"的支付方式扩展机制，未来新增支付渠道无需进行代码二次开发，能更好地支持业务需求。通过阿波罗配置实现支付参数的灵活管理和快速迭代，目前已接入微企付、京东支付。
3. **无项目负责人，产品不了解一些交互和技术，主动承担技术负责人角色**

- 负责与三方支付渠道公司、转转客户端、转转小程序、采货侠客户端、采货侠小程序、上门小程序等多方的技术对接。系统梳理支付交互流程，确保各端支付功能的一致性和稳定性。将支付交互流程、技术对接细节等系统梳理并沉淀为文档，确保后续维护和扩展的便捷性。

- 建立跨部门、跨公司的沟通群，主动对接各方开发人员，推动项目高效推进。在项目过程中，帮助客户端和小程序开发人员梳理关键技术问题，提炼最佳解决方案。

- 前端技术负责人

  - 前端技术团队的管理和协调工作。

  - 负责制定前端技术发展路线和规划，指导团队成员完成项目任务，确保项目按时交付并达到预期的质量标准

  - 与其他部门的负责人和团队密切合作，协调前后端技术的整合和交流，确保项目的整体顺利进行。

- 需求质量把控

  - 代码质量：结构清晰、逻辑严谨、可维护性强的代码

  - 兼容性和性能

  - 安全性

  - 测试和调试：确保功能正常、界面美观、交互流畅，及时修复bug和问题，保证项目质量。

  - 与设计和后端的协作：密切合作，确保前端页面与设计保持一致，前后端数据交互正常，功能实现符合需

## sentry

- **背景**

  - 前端错误监控方案Sentry 是一个开源的实时错误追踪系统，可以帮助开发者实时监控并修复异常问题。对团队来说，线上质量和处理问题的效率很重要。无法辅助解决问题

  - 收集信息混乱（定位问题慢，没有合理的错误等级划分无法确认问题严重程度及类型）

  - 部分监控缺失（接口，http）

  - 没有处理错误的标准和规范

  - 无法辅助解决问题

- 目标

  - 成为日常辅助我们发现、解决项目问题的工具

  - 制定问题分级规则、问题处理标准

  - 解决存量问题

- **改造**

  - SDK 提供 beforeSend 钩子，在发送错误或消息事件之前调用该钩子，可用于修改事件数据以删除敏感信息。

- **主要工作**

  - 解决存量问题——负责中台和平台重要项目sentry的治理，每周跟进，把控治理进度。

    - 1、项目问题数减少到20以下

    - 2、收集问题及原因

    - 3、每周组内过项目问题（机器人提醒）

    - 4、每周记录问题状态，邮件汇报

  - 分析问题上报有效性

    - 5、存量问题（解决/有结论/无影响）

    - 6、及时关注新增问题

    - 7、分析问题类型（代码错误-优化，接口/sdk-有效信息帮助优化项目，三方浏览器——过滤，基础包，特殊场景）

    - 8、分析上报合理性

  - 优化上报信息

    - 9、优化sentry上报规则

    - 10、增加上报信息（traceid等）

- 收益

  - 能监控真实问题 （监测到低版本安卓白屏）

  - 中台&平台项目错误个数 < 20

  - 帮助解决线上问题

  - 团队形成意识，及时关注项目异常情况 （每周都会组内过sentry问题、error企微提醒）

  - 完善错误等级划分，报警更准确。

- **错误类型**

  - 代码错误：try...catch、window.onerror

  - 资源加载错误：object.onerror: dom对象的onerror事件、performance.getEntries()、Error事件捕获

  - 图片加载错误：performance.getEntries()

- **异常捕获**

  - 全局捕获

    - 通过全局的接口，将捕获代码集中写在一个地方。接口：window.addEventListener(‘error’)  ；window.addEventListener(“unhandledrejection”)；document.addEventListener(‘click’) 等

    - 框架级别全局监听。

      - 监控JavaScript运行时错误（包括语法错误）和 资源加载错误
        语法错误   window.onerror = function(message, source, lineno, colno, error) { ... } 
        资源加载错误  window.addEventListener('error', function(event) { ... }, true)

      - promise
        window.addEventListener("unhandledrejection", event => {  
        ​console.warn(`UNHANDLED PROMISE REJECTION: ${event.reason}`);});

      - 拦截方法，调用前处理（trycatch）setTimeout、setInterval、requestAnimationFrame

      - axios中使用interceptor

      - vue：Vue.config.errorHandler

      - React：ErrorBoundary。static getDerivedStateFromError() 或componentDidCatch(error, info)中可以捕获

    - 全局函数封装包裹

    - 对实例方法重写，在原有功能基础上包裹一层

  - 单点捕获

    - 业务代码包裹

    - try catch

    - 写一个函数收集异常，异常发生调用

    - 写一个函数包裹异常，发生可以捕获

在工作中，我始终以解决实际问题为导向，注重细节和用户体验。面对复杂问题，我会冷静分析，积极寻找解决方案。我相信自己的项目经验和解决问题的能力，能够为贵公司前端开发工作贡献力量，非常期待能加入贵团队。
# 移动端优化

**网络优化**

1. **资源压缩与合并**
   - 代码压缩(JS/CSS/HTML)
   - 图片压缩和合适的格式选择(WebP/AVIF)
   - 合理的文件合并策略
2. **缓存策略**
   - 浏览器缓存(Cache-Control)
   - Service Worker缓存
   - CDN缓存：CDN（Content Delivery Network，内容分发网络）是指通过在不同地理位置部署服务器，来更快、更可靠地向用户分发静态和动态网页内容的技术。CDN的作用是：加速网站访问速度，提高用户体验，降低服务器负载，提高内容的可用性和安全性。
3. **按需加载**
   - 路由懒加载
   - 组件动态导入
   - 图片懒加载

**渲染优化**

1. **关键渲染路径优化**
   - CSS放头部，JS放底部
   - 内联关键CSS
   - 异步加载非关键资源
2. **减少重排重绘**
   - 使用transform替代位置改变
   - 批量DOM操作
   - 合理使用will-change
3. **虚拟列表**
   - 长列表分页或虚拟滚动
   - 避免一次性渲染大量DOM

**代码层面优化**

1. **JavaScript优化**
   - 防抖节流
   - Web Worker处理密集计算
   - 避免内存泄漏
2. **框架层优化**
   - 合理的组件拆分
   - 响应式数据优化
   - 使用SSR/SSG

**构建优化**

1. **打包优化**webpack**
   - Tree Shaking：移除未使用代码，见小宝体积
   - 代码分割(Code Splitting)：使用SplitChunksPlugin实现代码分割按需加载。
   - 压缩代码：TerserPlugin压缩js，css-minimizer-webpack-plugin压缩css
   - 异步加载
2. **现代化构建**
   - ESBuild/SWC加速构建
   - 并行构建
   - 增量构建

**监控与分析**

1. **性能指标监控**
   - FCP/LCP/TTI等指标 // 首次内容绘制/最大内容绘制/可交互时间
   - 错误监控
   - 用户行为分析
2. **持续优化**
   - 性能预算
   - CI/CD中的性能检测
   - A/B测试验证

# 图片的懒加载和预加载

预加载：提前加载图片，当用户需要查看时可直接从本地缓存中渲染。

懒加载：懒加载的主要目的是作为服务器前端的优化，减少请求数或延迟请求数。

两种技术的本质：两者的行为是相反的，一个是提前加载，一个是迟缓甚至不加载。
懒加载对服务器前端有一定的缓解压力作用，预加载则会增加服务器前端压力。

# 虚拟列表

**只渲染用户可见区域的元素**，三个关键步骤

1. **可视区域计算**：监听容器的滚动事件，结合容器高度和滚动位置，计算当前哪些数据在可视区域。

   ```javascript
   const scrollTop = this.$el.scrollTop;
   const startIndex = Math.floor(scrollTop / itemHeight);
   const endIndex = startIndex + visibleCount;
   ```

2. **动态渲染**：只渲染可视区域内的元素

3. 用一个占位元素填充整个列表高度，确保滚动条正常工作。

```javascript
<div class="virtual-list" @scroll="handleScroll">   
  <div class="placeholder" :style="{ height: totalHeight + 'px' }"></div>   
	<div class="content" :style="{ transform: `translateY(${offset}px)` }"> 
    <!-- 只渲染 visibleItems -->   
  </div> 
</div>
```

位置偏移：使用 CSS 的`transform`属性将渲染的元素 “移动” 到正确位置，避免重新计算布局：

```javascript
offset = startIndex * itemHeight; // 计算偏移量
```

**优化**：

​	缓冲区：可视区域上下额外渲染 5-10 个元素，减少滚动时的重渲染

​	DOM 复用：通过组件池复用已渲染的 DOM 节点

**库**：

- **Vue**：`vue-virtual-scroller`
- **React**：`react-window` 或 `react-virtuoso`
- **原生 JS**：`simple-virtual-list`

# 封装组件

**高内聚低耦合、可复用、可维护**的原则

1. **Props 设计**：明确核心功能和变体
2. **事件和插槽**：提供灵活交互和内容扩展
3. **样式与状态管理**：scoped CSS 避免样式污染；内部状态封装在内，外部通过props传
4. **工程化支持**：编写文档使用说明示例，测试常见场景

**如何灵活？**优先满足80%的场景，必要参数通过props。复杂场景通过插槽或者回调实现。复杂组件通过组件组合实现。

# 单页面应用/多页面应用

- SPA：使用单个 HTML 完成多个[页面切换](https://so.csdn.net/so/search?q=页面切换&spm=1001.2101.3001.7020)和功能的应用。只有一个 html 文件作为入口，一开始只需加载一次 js,css 等相关资源。使用 js 完成页面的布局和渲染。路由跳转，仅刷新局部资源。

- MPA：多个独立的页面的应用，每个页面必须重复加载 js,css 等相关资源。多页应用跳转，需要整页资源刷新。

- 区别<img src="https://api2.mubu.com/v3/document_image/28886397_b117b319-0842-4728-e39a-6b993114abd4.png" alt="img" style="zoom: 33%;" />

# 项目难点-技术服务业务例子

可编辑表格，自定义操作按钮，于是使用了editable. actionRender属性。编辑后获取表格的dataSource不是最新的。![img](https://api2.mubu.com/v3/document_image/28886397_dcbb69fc-2746-4080-fe80-342646672b12.png)

分析：

- Table文件中，列tableColumn相关计算使用了useMemo来缓存计算结果，其中的依赖项中没有actionRender。但是它的的处理也是在这个函数中，如果这个函数没有更新的话， 那actionRender中引用的state一直都会是旧值。

- 但是本身自带的onsave等都能拿到最新的state，对比发现actionRender中无 useRefFunction ，
  var actionCancelRef = useRefFunction(
  var actionRender = function actionRender

- 分析useRefFunction作用：通过 ref 将处理函数进⾏了保存，若给 actionRender 传⼊的是 ref.current ，然后在每次组件渲染时更新 ref.current 的指向，使得每次点击时都调⽤最新的 onClick。

- 改造：如果传入了自定义的actionRender，使用useRefFunction内部是时间处理可以访问最新的![img](https://api2.mubu.com/v3/document_image/28886397_ce4a9696-6485-41a0-c45d-1d27e21f0a64.png)
  https://github.com/ant-design/pro-components/pull/8547

# 攻击.方法XSS

- 跨站点脚本攻击XSS ：将恶意代码注入到应用中，浏览器去默认执行。
  Vue 和 React 等框架有针对其的策略。
   React DOM 在渲染所有输入内容之前，默认会进行转义。它可以确保在你的应用中，永远不会注入那些并非自己明确编写的内容。所有的内容在渲染之前都被转换成了字符串
- SQL 注入：攻击操纵 数据库查询 以获得未经授权的数据库访问，以执行恶意活动，例如损坏数据库或窃取敏感数据。
  防范：前端输入字段经过正确验证和处理。防止用户在输入的字段中插入恶意代码。
  后端也需要进行验证，同时通过一些工具来检测SQL注入
- 跨站点请求伪造 (CSRF) ：通过伪装的表单、链接或按钮，诱导用户更变敏感数据
  防范：验证码、使用CSRF Token、检查Referer、~~使用从服务器生成的 CSRF 令牌。.NET等来框架的内置 CSRF 来防。~~
- 中间人 (MitM)：利用不安全的通信通道（公共wifi等），监视更改用户-服务器的信息传输。
  安全互联网；不连公共wifi；HTTPS 和 TLS 等安全通信协议。
- 点击劫持：假的蒙层，诱骗用户点击与他们认为完全不同的内容
  X-Frame-Options标头，它可以确保你的网站不会嵌入到其他网站或 IFrame 中。
- 安全配置错误
  https://juejin.cn/post/7355798869110194195
- 依赖性利用

# axios取消

- **CancelToken**（旧版）：兼容性好，通过 `source.cancel()` 取消。

```javascript
const CancelToken = axios.CancelToken;
const source = CancelToken.source();

// 发送请求，传入 cancelToken
axios.get('/api/data', {
  cancelToken: source.token
})
.then(response => {})
.catch(error => {
  if (axios.isCancel(error)) {
    console.log('请求已取消:', error.message);
  } else {
    console.log('请求错误:', error);
  }
});
// 取消请求（可在任何地方调用）
source.cancel('用户取消请求');
```

- **AbortController**（新版）：基于 Web API，代码更简洁，通过 `controller.abort()` 取消。

```javascript
const controller = new AbortController();
axios.get('/api/data', {
  signal: controller.signal // 关联 AbortController 的 signal
})
.then(response => {})
.catch(error => {
  if (error.name === 'AbortError') {
    console.log('请求已取消');
  } else {
    console.log('请求错误:', error);
  }
});
// 取消请求
controller.abort();
```



# HTTP状态码

302:临时重定向，可能改变请求方法

303:临时重定向，强制使用get

307:临时重定向，保持请求方法不变

# HTTPS的加密原理

首先客户端发送请求到服务器，服务器给客户端颁发证书，且把自己的公钥和证书一起发送给客户端。证书是有CA私钥加密，客户端使用CA的公钥验证，验证成功后，客户端自己生成一个随机数预主密钥，然后用服务端的公钥加密后，发送给服务端，然后客户端和服务端根据预主密钥等条件生产会话秘钥。后续会话都使用会话密钥加密传输

# webpack和vite的区别

构建速度： webpack 需要将项目所有的资源，进行静态分析，生成分析依赖图，进行打包。冷启动时间长，热更新的时候需要重新构建依赖图，热更新也慢。 vite 是基于现代浏览器对于原生ES的支持，无需预先打包。冷启动时间短，只更新修改的模块，无需重新构建，且利用浏览对于es的缓存，使得热更新更快。

开发和生产模式： webpack 在开发和生产环境使用相同的打包机制 vite 开发环境使用原生es，按需编译。生产环境使用Rollup进行打包，生成优化的静态文件

生态： webpack 插件丰富，可以处理各种资源类型。社区活跃。 vite 生态相对较新，但是发展迅速，插件是基于Rollup。

