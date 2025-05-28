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

# 跨域

- 浏览器不能执行其他网站脚本，是因为“同源策略”

- **同源策略**：浏览器对js的限制，协议+域名+端口

- 解决方案（避开这种限制）

  - JSONP

    - <script>标签中src属性的链接可以访问跨域脚本

    - src链接必须带自定义函数名去接受返回数据
      http://local host:3000/?callback=getData

    - 缺点

      - 只支持get请求，传输数据有限

  - CORS跨域资源共享

    - 使用XMLHttpRequest发送请求，不符合同源，会在请求头加Orgin（协议域名端口）；服务器判断Origin是否在许可范围，接受请求后加响应头Access-Control-Allow-Origin；浏览器判断是否有Origin，有责处理数据，无责oneError捕获

    - 方法：服务器端设置Access-Control-Allow-Origin响应头

  - proxy代理

  - window.postMessage()

- cdn不受限制？

  - **静态资源（如 CSS、JS、图片）的跨域请求**在现代浏览器中是被**默认允许**的（除非服务器显式禁止）。因为它们不包含敏感数据，cookie等

- cdn和主站共用域名。

  - **限制场景**：cdn js访问敏感数据。浏览器对跨域js有更严格控制，防止注入攻击。主站启用 CSP（Content Security Policy），会显式指定允许加载资源的域名，其它不行。


# Cookie,LocalStorage,sessionStorage

- webstorage = LocalStorage,sessionStorage，只能存储字符串类型的数据

- 存储在客户端

- 大小：cookie（4k），sessionStorage & LocalStorage（5M+）

- 过期时间：cookie（设置的），LocalStorage（永久），SessionStorage（浏览器关闭，同一域名下的不同窗口 / 标签页之间数据不共享）

- 数据传输：cookie会传到服务器

- 属性

  - 存数据`localStorage.setItem('username', 'john');`

  - 取数据`localStorage.getItem('username')`，存在判断!== null

  - 删数据

    ```
    localStorage.removeItem('age'); // 删除指定键
    localStorage.clear(); // 清空所有数据
    ```

  - 遍历

    ```javascript
    localStorage.key(i)
    ```


# 浏览器渲染的线程都有哪些

- 主线程
  - 负责解析HTML、CSS、JavaScript
- 合成线程
  - 负责将页面分成多个图层，进行图层合成
- 光栅化线程
  - 负责将图层转换为位图，通常由GPU加速
- JavaScript引擎线程
  - 负责解析和执行JavaScript代码
- 事件处理线程
  - 负责处理事件循环，将事件分发给主线程或其他线程处理。
- 定时器线程
  - 负责处理定时器，如setTimeout、setInterval
- 网络请求线程
  - 负责处理网络请求，如XMLHttpRequest、fetch
- WebWorker线程 -允许在后台运行JavaScript代码，不阻塞主线程。
- serviceWorker线程
  - 用于实现离线缓存、推送通知等功能，独立于主线程运行。
- GPU线程
  - 负责处理GPU相关任务，如3D渲染、视频解码等。

# 页面渲染过程

- 浏览器输入Url

- 查找缓存：浏览器-系统-路由器

- DNS域名解析：浏览器向DNS服务器发起请求，解析Url的IP地址。DNS基于UDP

- 建立TCP链接：根据IP和端口和服务器建立TCP链接

- 发起Http请求：浏览器发起读取文件的Http请求，请求报文是第三次握手的数据

- 服务器响应请求返回结果：服务器对浏览器请求响应，发送html给浏览器

- 关闭TCP链接：四次挥手

- 浏览器渲染：浏览器解析html内容并渲染

  - 构建DOM树

  - 构建CSS树

  - 构建render树：浏览器将DOM和CSS结合

  - 布局：计算每个节点在屏幕位置

  - 绘制：遍历render树，使用UI后端层绘制每个节点
- 执行javascript
- 解析和执行javascript代码，可能会修改DOM或者CSSOM，引起重新布局和绘制
- 页面交互
- 关闭连接

# 重绘，重排

- 重绘：元素外观改变，布局没变

- 重排：DOM变化影响元素几何信息，浏览器需要重新计算几何信息并放在正确位置。重新生成布局

- 如何避免：

  - 集中改变样式

  - 节点属性值不要放在循环里做变量

  - fixed，position：absoult。

  - 不使用table布局

  - 动画使用GPU，translate使用3d变化

  - 提升为合成层（好处：GPU快，只重绘本身，方法：will-change: transform）

# 防抖，节流

防抖：函数频繁触发，当停止触发后空闲一段时间后执行一次。
(回城被打断)
1秒内。只要有新的触发产生：从0开始计时。

```javascript
function debounce(fn, interval = 300) {
    let timeout = null;
    return function () {
        clearTimeout(timeout);
        timeout = setTimeout(() => {
            fn.apply(this, arguments);
        }, interval);
    };
}
```

节流：指定时间间隔内只会执行一次任务。
(技能冷却中)
1秒内。只要有新的触发产生：无效，除非之前的操作执行完。

```javascript
function throttle(fn, interval = 300) {
    let canRun = true;
    return function () {
        if (!canRun) return;
        canRun = false;
        setTimeout(() => {
            fn.apply(this, arguments);
            canRun = true;		//可以执行下一次的循环了
        }, interval);
    };
}
```

应用场景
防抖在连续的事件，只需触发一次回调的场景有：
搜索框搜索输入。只需用户最后一次输入完，再发送请求
手机号、邮箱验证输入检测
窗口大小resize。只需窗口调整完成后，计算窗口大小。防止重复渲染。

节流在间隔一段时间执行一次回调的场景有：
滚动加载，加载更多或滚到底部监听
搜索框，搜索联想功能

# 强缓存/协商缓存

- 浏览器缓存：应答模式<img src="https://document-image.mubu.com/document_image/B691F60FA2024B8A1716629817.jpg" alt="img" style="zoom: 25%;" />
- 在浏览器缓存机制中，强缓存和协商缓存是两个核心概念，它们能有效减少对服务器的请求，从而提升页面加载速度，减轻服务器压力。
- 强缓存（200（from disk cache 字体和大css/ from memory cache图片和脚本））

  - 从本地缓存中读取资源，根据缓存规则决定决定是否使用缓存结果。请求头Expires（优先级高）和Cache-control<!--max-age=100后过期；no-cache：协商缓存；no-store：不用缓存；public：所有用户都能请求；private：只单个用户浏览器缓存，代理不能访问-->

  - 分类

    - 不存在结果和标识，强缓存失效。直接向服务器发请求

    - 存在结果和标识，但结果失效，使用协商缓存

    - 存在结果和标识，结果有效，使用强缓存，返回200
- 协商缓存（304）

  - 强缓存失效后，会先向服务器发送一个请求，询问服务器该资源是否有更新。浏览器携带缓存标识向服务器发送请求，服务器根据缓存标识判断是否使用缓存。

  - 响应头last-modified 请求的时候带if-modifie-since，最后一次文件修改的时间（s）
    首次请求，服务器会在响应头添加 Last-Modified。再请求if-modifie-since就是 Last-Modified。最后修改时间<if-modifie-since,304无修改。大于200更新

  - 响应头 Etag 请求的时候头部 if-none-match，比较资源内容是否改动（优先级高，资源的唯一标识）
    首次请求的时候，服务器会返回etag。再请求If-None-Match 就是etag的值。不相等，资源更新；相等取缓存304

  - 分类

    - 生效，返回304

    - 失效，返回200和结果

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

# Fiber

### **1. 为什么需要 Fiber？**

- **旧版问题**：React 15的渲染是**同步递归**的， 协调器（Reconciler）通过递归方式同步构建和对比虚拟 DOM 树，若遇到复杂组件或大规模 DOM 更新时会**长时间阻塞主线程**，导致用户操作（如点击、滚动）无响应，页面卡顿。

### **2. Fiber 架构通过三大核心改进优化了这一过程：**

**① 任务切片：把大任务拆成小任务**

- 做法：
  - 将虚拟 DOM 树拆解为 **Fiber 节点链表**（每个节点是一个小任务）。
  - 渲染时不再一次性递归完整个树，而是**每次只处理一个 Fiber 节点**，处理完就暂停。
- 好处：
  - 主线程不会被长时间占用，可及时响应其他操作（如用户点击）。

**② 调度器：智能分配时间和优先级**

- 时间分片：
  - 把主线程时间划分为多个 **“时间片”**（但个任务在一帧内最大执行时间）。
  - 每个时间片内执行一部分任务，超时就暂停，让浏览器有时间渲染页面。
  - 类比：就像挤地铁，每次车门开的瞬间（浏览器空闲）挤进去一点人（执行一点任务），车门要关了就停下（暂停）。
- 优先级管理：
  - 为不同任务分配优先级（如用户交互 > 数据加载 > 低优先级更新）。
  - 高优先级任务（如点击事件）可中断低优先级任务，优先处理。
- 协作式调度：
  - 任务执行过程中可暂停、恢复、调整顺序，类似多人协作分工。

**③ 增量渲染与双缓存：高效更新 DOM**

- **增量渲染**：
  - 协调器（Reconciler）分阶段构建 Fiber 树，标记需要更新的节点（如新增、删除）。
  - 然后，渲染器（Renderer）最后**批量更新真实 DOM**，减少重排和重绘次数。
- **双缓存机制**：
  - 内存中同时维护两棵 Fiber 树：
    - **current Fiber**：当前显示在页面上的。
    - **workInProgress Fiber**：正在计算的新树。
  - 计算完成后，直接切换两棵树，实现无缝更新。如果出错，可回滚到旧树。

### 3. 下一个要执行的 Fiber 任务呢

- 使用 深度优先遍历 + 链表指针：
  1. 先处理当前节点（比如 `<div>`）。
  2. 如果有子节点（如 `<div>` 里的 `<p>`），优先处理子节点。
  3. 子节点处理完，通过 `sibling` 指针找下一个兄弟节点（如 `<p>` 的兄弟 `<span>`）。
  4. 兄弟节点都处理完，通过 `return` 指针回到父节点。

- 类比：就像玩游戏时，先通关当前关卡的所有小 BOSS（子节点），再打下一个关卡（兄弟节点），打完所有关卡回主城（父节点）。

### 4. 如何中断和恢复

- Fiber 架构通过 **全局指针** 和 **链表结构** 实现任务的中断和恢复：
  1. **全局指针**：`workInProgress` 指向当前正在处理的 Fiber 节点
  2. **中断时**：保存 `workInProgress` 指针
  3. **恢复时**：从 `workInProgress` 指针指向的节点继续执行

- 怎么知道结束了？
  - `workInProgress` 指针为 `null`（表示没有待处理的工作单元）
  - 所有 Fiber 节点的副作用（如 DOM 更新）已收集到 `effectList` 中


### 5. Fiber 的工作阶段：render 阶段和 commit 阶段

- render 阶段：构建 Fiber 对象，构建链表，在链表中标记要执行的 DOM 操作 ，可中断。

- commit 阶段：根据构建好的链表进行 DOM 操作，不可中断。

# react diff

React的Diff算法是一种用来高效更新页面的机制。简单来说，当你修改React组件的数据时，它不会直接去操作真实的DOM（因为DOM操作很慢），而是先在内存里对比新旧“虚拟DOM”的差异，只更新需要变化的部分。

 这个对比过程有三个关键策略： 

1. **树形比较**：React只会比较同一层级的DOM节点。比如，如果你把一个节点从父节点A移到父节点B，React不会识别出这是“移动”，而是会直接删A建B。所以尽量避免跨层级移动节点。 
2. **组件比较**：对于React组件，类型相同只更新组件内部变化的部分；类型不同（比如从`<Button>`变成了`<Input>`）就直接整个替换掉。你还可以通过`shouldComponentUpdate`这个函数来手动控制组件是否需要更新。
3. **元素比较**：当处理列表元素（比如用`map`渲染多个子元素）时，React需要你给每个元素一个唯一的`key`（比如ID）。这样它就能知道这些元素是增删改？。如果不用key，React默认会按顺序比较元素，一旦列表顺序变了（比如插入一个新元素），就可能导致性能问题或显示错误。 

另外，React 16之后引入了Fiber架构，把这个对比过程变成了“可打断的”。也就是说，它不会一次性算完所有差异，而是拆分成很多小任务，这样不会阻塞浏览器渲染页面，用户体验会更好。

整个更新过程分成两个阶段：第一阶段计算差异生成 workInProgress Fiber 树（可打断render），第二阶段实际更新DOM（不可打断commit，执行生命周期钩子（如 `componentDidMount`）和副作用（如 useEffect））。 

最后，使用Diff算法时要记住：给列表元素加稳定的key（别用index），避免跨层级移动节点，合理使用`React.memo`或`shouldComponentUpdate`来减少不必要的比较，这样你的React应用会跑得更快。O (n³) 复杂度降至 O (n）



# class组件和函数组件

- class：基于es6的class定义组件，接收props，返回react元素。它是数据和逻辑的封装。 也就是说，组件的状态和操作⽅法是封装在⼀起的。

- 函数：主要就是返回一个值。数据和操作是隔离的。函数就是返回组件的 HTML 代码，返回结果只依赖于它的参数。不改变函数体外部数据、函数执⾏过程⾥⾯没有副作⽤。

- class缺点

  - 难拆分、难测试

  - 业务逻辑分散在各个组件中，会冗余。

  - 引入了复杂编程，render props

  - this

- 区别

  - 函数组件性能高
    class需要实例化，函数只需要执行返回结果即可

  - 函数：无状态组件（实例，state，生命周期，this），纯函数，依赖props

  - 调用方式

    - 函数：重新调用方法返回新的react元素

    - class：new一个新的实例（this是可变的），然后render返回react元素。

    - 操作中改变状态值，函数会按照顺序返回状态。class会直接获取到最新的状态

  |              | 函数                | class |
  | ------------ | ------------------- | ----- |
  | 编写方式     |                     |       |
  | 状态管理     | hooks出现前，无状态 |       |
  | 生命周期     | 无                  |       |
  | 调用方式     |                     |       |
  | 获取渲染的值 |                     |       |

  

# 函数组件模拟生命周期

```javascript
// componentDidMount()  // componentWillUnmount() 
useEffect(() => {
    console.log('Component mounted');
    // 在这里执行挂载后的操作，类似于 componentDidMount
    return () => {
      console.log('Component will unmount');
      // 在组件即将卸载时执行清理操作
    };
  }, []); // 第二个参数是空数组，表示只在组件挂载和卸载时执行
```

```javascript
// componentDidUpdate() 可以比较前后的 props 或 state 变化
import React, { useEffect, useState } from 'react';
function MyComponent(props) {
  const [data, setData] = useState(props.data);
  useEffect(() => {
    console.log('Component updated');
    if (data !== props.data) {
      console.log('Data changed');
    }
  }, [data, props.data]);
  return (
    <div>
      <button onClick={() => setData('New Data')}>Change Data</button>
    </div>
  );
}
```

# hooks （react16.8新增）

- 好处：

  - 为函数组件赋能，让函数组件能处理状态和副作用（除了正常渲染处理数据外的事，修改dom，请求数据等）
  - 解决class组件逻辑复用困难，避免高阶组件嵌套
  - 摆脱this
  - 代码是按功能聚合，不是生命周期，可读性和可维护性较高。

- 必须在函数组件内使用，因为它依赖react上下文

- **useState()** //状态钩⼦

  - 管理 state，让函数组件具有维持状态的能力

  - state 中永远不要保存可以通过计算得到的值（url，props，cookie，loacalstorage）

  - class和函数组件的区别

    - 类组件中 setState 只能有一个，一个对象，不同的属性来标识不同状态

    - setState 可有多个，更加语义化，更加方便使用。

- useReducer() 复杂状态管理  ，状态转换机器

  - action：发生什么；dispatch：发送给reducer；reducer：处理state；返回一个新的state

  <img src="/Users/burst/Library/Application Support/typora-user-images/image-20250526155534509.png" alt="image-20250526155534509" style="zoom:25%;" />

  - 优势： 

    - 处理复杂状态逻辑（对象、依赖关系等，更新逻辑会分散到很多地方），会将状态和更新逻辑集中，可以和ui分离开。
    - 可读性、可和维护性。可测试性（可以直接给reducer函数各种state组合测试）

  - 注意：不能影响外部（api，dom操作等）；不能直接改state，需返回全新状态（对象可能会因为修改的是引用地址检测不到更新）。

  - ```javascript
    const counterReducer = (state, action) => {
      switch (action.type) {
        case 'increment':
          return { count: state.count + 1 };
        case 'decrement':
          return { count: state.count - 1 };
        case 'reset':
          return { count: action.payload }; // payload 是可选的额外数据
        default:
          throw new Error('未知 action');
      }
    };
    const [state, dispatch] = useReducer(counterReducer, { count: 0 });
    <button onClick={() => dispatch({ type: 'increment' })}>+1</button>
    ```

- **useContext()** //共享状态钩⼦

  - 通过context实现跨层级共享状态

    ```javascript
    //父
    const FatherContext = React.createContext('light');
    <FatherContext.Provider  value={{ currentUser, setCurrentUser }}>      
        <Toolbar />    
    </FatherContext.Provider>
    //子
    const { currentUser, setCurrentUser } = useContext(FatherContext);
    ```

- **useEffect()** //副作⽤钩⼦

  - useEffect是会在整个⻚⾯渲染完才会调⽤的代码

- **useLayoutEffect**

  - 在react完成DOM更新后⻢上同步调⽤的代码，会阻塞⻚⾯渲染。componentDidMount&componentDidUpdate

- **useRef** 保存引⽤值

  - 主要用于获取 DOM 节点、存储不影响渲染逻辑的变量，以及在多次渲染之间保持数据。
  - `ref` 只是一个普通对象，其<u>变化不会触发渲染</u>
  - 可以通过 ref.current 值访问组件或真实的 DOM 节点，重点是组件也是可以访问到的，从⽽可以对 DOM 进⾏⼀些操作

- **useImperativeHandle**

  - 自定义通过 ref 暴露给父组件的实例值

  - 让⽗组件获取⼦组件内的索引

    ```javascript
    // 父
    <SearchHistory ref={historySearch} />
    historySearch.current?.submit()
    ```

    ```javascript
    //子
    const SearchHistory = forwardRef((props, ref) => {
      useImperativeHandle(ref, () => ({
        submit: () => { /* ... */ }
      }));
      return <div>
    });
    ```

- **useCallback** 缓存函数，避免子组件不必要渲染

  - ~~函数组件转class组件的语法糖。重新渲染时，函数组件会将代码全都执行，方法会重新生成的。usecallback会缓存一个方法，重新渲染时不会重新生成。~~

  - ```javascript
    const memoizedCallback = useCallback(() => { doSomething(a, b) }, [a, b],);//依赖项发生变化时才重新创建函数
    ```

  - 使用场景：子组件使用 `React.memo` （缓存组件的渲染结果）时才有明显效果；性能瓶颈处使用

    ```javascript
    const MyComponent = React.memo(function MyComponent(props) {
      /* 使用 props 渲染 */
    });
    ```

- **useMemo** 缓存高开销的计算结果

  - `const memoizedValue = useMemo(() => computeExpensiveValue(a, b), [a, b]);//依赖项发生变化时才重新计算`
  - props可以控制子组件渲染
  - useCallback 不会执⾏第⼀个参数函数，⽽是将它返回给你，⽽ useMemo 会执⾏第⼀个函数并且将函数执⾏结果返回给你。


## hooks比class好处

| class                                                        | hooks                                                    |
| ------------------------------------------------------------ | -------------------------------------------------------- |
| `this` 指向混乱、构造函数冗余                                | 无需绑定this，无需构造函数，消除样板化代码               |
| 相关逻辑分散在不同生命周期方法中，如 `componentDidMount` 和 `componentWillUnmount` | `useEffect` 将相关逻辑放在一起                           |
| 高阶组件和 render props 导致组件嵌套过深（"嵌套地狱"）。     | 自定义 Hook 提取可复用逻辑                               |
| 复杂的类型定义（如 `this` 的类型、生命周期方法的类型）       | 与ts更好集成，自动推导类型，减少模板代码                 |
| shouldComponentUpdate和 `React.PureComponent` 只能进行浅比较 | 更细粒度的渲染控制React.memo` + `useCallback` + `useMemo |
| 依赖 `this` 和生命周期方法，测试时需要模拟组件实例           | 纯函数，容易测试                                         |
|                                                              | 学习成本小                                               |

# useState为什么不能放判断里

**核心限制原因**

- **链表结构依赖顺序**：React 通过调用顺序（链表索引）来关联状态和 Hooks。if会导致状态与变量完全错乱。
- **多次渲染的一致性**：必须保证每次渲染时 Hooks 的调用顺序完全相同。（React 在 **开发模式** 中会维护一个 `renderPhaseHooks` 数组，用于验证 Hooks 调用顺序，`renderPhaseHooks` 的长度会与预期不符，React 会抛出警告："Invalid hook call. Hooks must be called in the exact same order in every render."）
- **性能优化**：避免动态创建和销毁 Hooks 对象，提高渲染效率。

# react组件通信

- ⽗组件向⼦组件通信：props传递数据or函数

- ⼦组件向⽗组件通信：父定义callback，通过props传递子组件，子组件将要传递的子通过callback传

- 状态提升（兄弟组件通信）：将共享状态提升到最近的共同父组件，通过 props 传递数据和回调

  ```javascript
  // 父组件 
  function Parent() {  
    const [count, setCount] = useState(0);    
    return (<div><IncrementButton onIncrement={() => setCount(count + 1)} />
  					<DisplayCount count={count} />    </div>  ); } 
  // 兄弟组件1 
  function IncrementButton({ onIncrement }) {  return <button onClick={onIncrement}>Increment</button>; } 
  // 兄弟组件2 
  function DisplayCount({ count }) {  return <p>Count: {count}</p>; }
  ```

- Context API（跨层级通信）：创建context组件ThemeContext，provide一个value，深层子组件可以通过useContext(ThemeContext)取到value

  ```javascript
  // 创建 Context
  const ThemeContext = React.createContext();
  // 提供者组件
  function App() {
    const [theme, setTheme] = useState('light');
    
    return (
      <ThemeContext.Provider value={{ theme, setTheme }}>
        <Header /> {/* 深层子组件 */}
      </ThemeContext.Provider>
    );
  }useReducer + Context（轻量级状态管理）
  // 深层子组件
  function Header() {
    const { theme } = useContext(ThemeContext);
    
    return (
      <header className={theme}>
        <h1>Welcome</h1>
      </header>
    );
  }
  ```

- EventBus：定义个全局事件总线，eventBus.emit发送 ，on接收。

  ```javascript
  // 创建事件总线 
  class EventEmitter {  
    constructor() {    this.events = {};  }    
    on(event, callback) {    this.events[event] = (this.events[event] || []).concat(callback);  }    
    emit(event, data) {    (this.events[event] || []).forEach(callback => callback(data));  } 
  } 
  const eventBus = new EventEmitter(); 
  // 发送组件 
  function Sender() {  const sendData = () => {    eventBus.emit('data', 'Hello from sender!');  };    return <button onClick={sendData}>Send</button>; } 
  // 接收组件 
  function Receiver() {  useEffect(() => {    const handler = (data) => console.log('Received:', data);    eventBus.on('data', handler);        return () => eventBus.off('data', handler); // 清理  
  }, []);    return <div>Listening for data...</div>; }
  ```

- 状态管理库（Redux/MobX/Recoil）

- useReducer + Context（轻量级状态管理）

  ```javascript
  // 创建 Context
  const CounterContext = React.createContext();
  
  // 定义 reducer
  const counterReducer = (state, action) => {
    switch (action.type) {
      case 'INCREMENT':
        return state + 1;
      default:
        return state;
    }
  };
  
  // 提供者组件
  function CounterProvider({ children }) {
    const [count, dispatch] = useReducer(counterReducer, 0);
    
    return (
      <CounterContext.Provider value={{ count, dispatch }}>
        {children}
      </CounterContext.Provider>
    );
  }
  
  // 使用组件
  function CounterDisplay() {
    const { count } = useContext(CounterContext);
    
    return <p>Count: {count}</p>;
  }
  ```

  

- refs（DOM 引用与组件通信，父子）

- 路由参数

- WebSocket

  ```javascript
  function ChatRoom() {
    const [messages, setMessages] = useState([]);
    useEffect(() => {
      const socket = new WebSocket('ws://example.com');
      socket.onmessage = (event) => {
        setMessages(prev => [...prev, JSON.parse(event.data)]);
      };    
      return () => socket.close();
    }, []); 
    const sendMessage = (text) => {
      socket.send(JSON.stringify({ text }));
    };  
    return (
      <div>
        {messages.map(msg => <p>{msg.text}</p>)}
        <input onKeyPress={sendMessage} />
      </div>
    );
  }
  ```

# redux

- Redux就是一个js容器，用于全局的状态管理

<img src="https://i-blog.csdnimg.cn/direct/69ee4d6ca43942ccb990c9e5dc6adedf.png" alt="img" style="zoom:25%;" />

- 为什么用？

​	React是单向数据流，数据就是父通过props传递，子父就是通过传递函数的方式来传递修改值。数据较复杂就要用

- 核心

  - 单一数据源。state存在reducer里，这个reducer只存在唯一store
  - state是只读的。改state通过action，store.dispatch(action)
  - 使用reducer来进行修改。

- 组成

  - store：

    ```javascript
    const store = createStore(reducer)  // createStore方法是redux提供的
    store.getState()：//获取reducer中返回的state数据；
    store.subscribe()：//用来注册监听state是否改变；
    store.dispatch()：//用于发送action，来修改reducer中的state数据；
    ```

  - reducer：是一个函数，接收state、action，生成新的state

    ```javascript
    const initState={...}
    export default (state=initState,action)=>{
    	const newState = JSON.parse(JSON.stringfy(state)) ; // 由于reducer不能直接修改state，所以做下深拷贝
    	if(action.type === XXX){
    		.....    // 这块就是针对不同的action type，对数据进行不同的处理，处理完后，将最新处理完后的nesState返回给store
    	}
    	return newState；
    }
    
    ```

  - action：js对象，有type表示执行的动作

- 使用场景

  - 获取其他组件的实时状态

  - 需要改变其它组件状态

  - 尽量不用

# setState()

# 生命周期()

# React15

- 使用循环递归虚拟DOM，使用js执行栈，需执行到任务完成为止。若虚拟dom树较深，会长时间占用主线程，此时无法进行其他操作，使页面卡顿。

# React16

- 使用循环来模拟递归，diff过程是占用浏览器的空闲时间，解决页面卡顿。

- 三层模型

  - Scheduler (调度层)：调度任务的优先级，高优任务优先进入协调器

  - Reconciler (协调层)：构建 Fiber 数据结构，比对 Fiber 对象找出差异, 记录 Fiber 对象要进行的 DOM 操作。（15是找差异立刻更新。）

  - Renderer (渲染层)：负责将发生变化的部分渲染到页面上。（16可中断，15不可）

# React19

- 创建了“React 编译器”。现在将管理这些重新渲染。React 将自动决定何时以及如何更改状态并更新 UI

- 服务器组件

  - 所有组件默认都是客户端的。只有当你使用 ‘use server’ 时，组件才是服务器组件

  - 优势：

    - SEO：服务器渲染的组件通过向网络爬虫提供更可访问的内容来增强搜索引擎优化。

    - 性能提升：服务器组件有助于更快地加载页面和改善整体性能，特别是对于内容密集型应用程序。

    - 服务器端执行：服务器组件使在服务器上执行代码变得无缝和高效，使诸如 API 调用之类的任务变得轻松。

- 动作：将让你将动作集成到 HTML 标签 中。
  原：<form onSubmit={search}>客户端上运行
  现：<form action={submitData}>在客户端或服务器端

- Web 组件： 在React 应用程序中利用现有的 Web 组件生态系统

- 文档元数据：直接在我们的 React 组件中使用 title 和 meta 标签

- 资源加载
  图像和其他文件将在用户浏览当前页面时在后台加载。这个改进应该有助于改善页面加载时间并减少等待时间。
  引入了用于资源加载的生命周期 Suspense，包括脚本、样式表和字体。这个特性使 React 能够确定内容何时准备好显示，消除了任何“未样式化”闪烁。

- React Hooks： 

  - 新的 use() 钩子：简化我们如何使用 promises、async 代码和 context
    const value = use(resource);

  - useFormState() 钩子：允许你基于表单提交的结果来更新状态。
    const [state, formAction] = useFormState(fn, initialState, permalink?);
    fn：当表单提交或按钮被按下时要调用的函数。
    initialState：你希望初始状态是什么值。它可以是任何可序列化的值。在首次调用后，此参数将被忽略。
    permalink：这是可选的。一个 URL 或页面链接，如果 fn 将在服务器上运行，则页面将重定向到 permalink。

  - useFormStatus()钩子
    const { pending, data, method, action } = useFormStatus();
    pending：如果表单处于挂起状态，则为 true，否则为 false。
    data：一个实现 FormData 接口的对象，包含父级 正在提交的数据。
    method：HTTP 方法 – GET 或 POST。默认情况下为 GET。
    action：一个函数引用。

  - useOptimistic() 钩子
    允许你在异步操作进行中显示不同的状态
    const [ optimisticMessage, addOptimisticMessage] = useOptimistic(state, updatefn)

# 避免react重复渲染的手段

- 使用React.memo() 包裹组件，缓存组件渲染结果
- 使用useMemo() 缓存复杂计算结果
- 使用useCallback() 缓存函数引用
- 使用useRef() 创建不变的引用对象
- 使用React.Fragment 包裹组件，避免额外DOM节点
- 使用React.StrictMode 包裹组件，检查潜在问题

# this

- 全局作用域：this是window（浏览器环境）、global（node环境）

- 函数指向window（严格模式undefined）；对象指向对象；构造函数指向新创建对象

- 箭头函数this是继承外部函数

- dom指向触发事件的元素

- call、apply 或 bind改变内部指向
  bind：返回一个新的函数，新函数的 this 指向被绑定为指定的值
  call、apply：立即调用函数，并且第一个参数是 this 的指向
  `​function.call(new,arg1, arg2, ...])`

  `fuction.bind(obj)`

  `function.apply(new, [arg1, arg2, ...])`

# bind，call，apply

```
Function.prototype.myBind = function(context, ...args) {
  const originalFunc = this

  return function(...newArgs) {
    const combinedArgs = args.concat(newArgs)
    const result = originalFunc.apply(context, combinedArgs)
    return result
  }
}
```

```
Function.prototype.myCall = function(context, ...args) {
  // 1. 处理 undefined 和 null 的上下文
  context = context || window; // 浏览器环境用 window，Node.js 需改为 globalThis
  // 2. 创建唯一键避免属性覆盖
  const fnKey = Symbol('__tempFn__');
  // 3. 将当前函数绑定到上下文
  context[fnKey] = this; // this 指向原函数
  // 4. 执行函数并保存结果
  const result = context[fnKey](...args);
  // 5. 清理临时属性
  delete context[fnKey];
  // 6. 返回执行结果
  return result;
};
```

```
Function.prototype.myApply = function(context, argsArray) {
  // 类型安全检查
  if (typeof this !== 'function') {
    throw new TypeError('调用者必须是函数');
  }
  // 处理上下文
  context = context != null ? Object(context) : window;
  // 创建唯一键
  const fnKey = Symbol('fn');
  // 绑定函数
  context[fnKey] = this;
  // 参数处理
  let result;
  if (!argsArray) {
    result = context[fnKey]();
  } else {
    if (!Array.isArray(argsArray) && !isArrayLike(argsArray)) {
      throw new TypeError('第二个参数必须为数组或类数组');
    }
    result = context[fnKey](...Array.from(argsArray));
  }
  // 清理
  delete context[fnKey];
  return result;
};
```

# new

1. 新建了一个空对象
2. 对象的（`__proto__`）属性指向构造函数的prototype 
3. 绑定this
4. 执行构造函数后返回这个对象

# 原型

是JavaScript语言中固有的特性

**原理**：对象引用了另一个对象来获取该对象的属性和方法。

prototype（原型）：通过调用构造函数而创建的所有对象实例的原型对象

每个函数都有 一个prototype 属性指向一个原型对象，原型对象包含特定类型的所有实例共享的属性和方法。

每个对象（除null）都有 `__proto__` 属性，这个属性指向了创建该对象的构造函数的原型。而原型对象也通过`__proto__`指向它自己的原型对象，层层向上直到Object.prototype，这样就形成了原型链。

是否是该对象的原生属性：teacher.hasOwnProperty('name')

**特点**：
当访问对象属性时，如果对象内部没有这个属性，就会沿着原型链一直往上找；
当修改原型时，与之相关的对象也会继承这一改变。
![在这里插入图片描述](https://img-blog.csdnimg.cn/2020073011130453.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2J1cnN0Z2lybHM=,size_16,color_FFFFFF,t_70)

Person.prototype.name 这种的写法是在原有的基础上把值改了。 改的是属性，也就是房间里面的东西。
而 Person.prototype={name:’ cherry’ }是把原型改了，换了新的对象。 改了个房间。_proto_指向的空间不变。

**构造函数、原型、实例之间的关系**

每个实例对象（ object ）都有一个私有属性（称之为 `__proto__ `）指向它的构造函数的原型对象（**prototype** ）。该原型对象也有一个自己的原型对象( `__proto__ `) ，层层向上直到一个对象的原型对象为 `null`。根据定义，`null` 没有原型，并作为这个**原型链**中的最后一个环节。

每个构造函数都有一个原型对象(prototype)，原型对象都包含一个指向构造函数的指针（constructor），而实例都包含一个指向原型对象的内部指针（`__proto__`）。

Object.create(原型);
Object.prototype 是原型链的终端

# 作用域let，const，var

- 变量与函数的访问范围

  - 全局作用域：在程序任何地方都能访问，eg：window属性

  - 函数作用域：固定代码片段使用

- 创建函数，即声明当前函数作用域（上下文）

- 作用：隔离变量

- 作用域链：变量在创建函数的作用域取值。没查到就去上级查，直到全局作用域。这个查找的过程链

- 变量

  |          | var  | let  | const |
  | -------- | ---- | ---- | ----- |
  | 块       | ❌    | ✅    | ✅     |
  | 先声明   | ❌    | ✅    | ✅     |
  | 重复声明 | ✅    | ❌    | ❌     |

  建议用let，const块级作用域替代闭包

# 闭包

- what

​	有权访问另一个函数作用域的中变量的函数

​	js变量作用域属于函数作用域，函数执行完，作用域会被清理，内存被回收。 闭包的函数是建立在内部子函数（闭包）上，它可以访问上级作用域，上级执行完，作用域也不会被清理。 

- 特性

  可以访问定义它们的外部变量

  保护：区域中私有变量不受外界影响，避免全局变量污染

  保存：将外部作用域中变量存储在内存中，而非函数

- 实现

  函数嵌套。eg：一个函数的返回值是另一个函数，即函数和它的执行环境形成了一个闭包

  ```
  function addFn() { 
  	let a = 1;
  	return function () {a++; return a;} 
  }
  let newFn = addFn();
  ```

  内部函数引用外部函数局部变量，延长外部变量生命周期

  <img src="/Users/burst/Library/Application Support/typora-user-images/image-20250528145910084.png" alt="image-20250528145910084" style="zoom:25%;" />

- 用途

  模仿块级作用域

  封装私有化变量

  **节流**：控制事件触发频率

  ```
  function throttle(fn, wait) {
  	let flag = false;
  	return function () {
  		if (flag == false) {
  			flag = true
  			timer = setTimeout(() => {
  				fn();flag = false;
  			}, wait);                
  		}           
  	}        
  }
  ```

  防抖：事件触发后，应在一定的时间后才能生效

  ```
  function debounce(callbackFn, interval) {
  	var flag = null            
  	return function () {                
  		clearTimeout(flag)                
  		flag=setTimeout(()=>{callbackFn()},interval)
  	}        
  }
  ```

- bad：内存泄漏

- good：延长局部变量生命周期

# 垃圾回收

- why：内存不释放，页面性能会变慢。即内存泄漏（全局变量、闭包、Dom元素引用、定时器）

- 浏览器有垃圾回收机制，定期找出不继续使用的变量来释放

- method: 标记清除

  - 变量进入执行环境，被“标记进入”。离开时被“标记离开”。会销毁离开的值并释放内存

  - google浏览器：不定时查找当前内存引用，无占用则清除

  - ie浏览器：引用计数。占用1次+1，移除-1。0时回收

- 优化：手动释放，内存优化，取消占用内存

# eventloop

- why

  js单线程，防止函数执行时间过长阻塞代码。

- 运行机制

  1、会先执行同步栈代码 2、执行异步队列中微任务(清空)， 3、执行宏任务 for（取一个宏，放进任务队列执行，执行微）。

- 宏任务

  ajax、setTimeout、setInterval、script

- 微任务

  promise.then、MutationObserver   process.nextTick

- node环境

  - 基于v8引擎运行在js环境

  - 比基本eventloop多：I/O、网络操作

  - 执行顺序

    - timer：setTimeout、setInterval

    - pending callback：调用上一次事件循环没在 poll 阶段立刻执行，而延迟的 I/O 回调函数

    - idle，prepare

    - poll：检索I/O，执行回调

    - check : 执⾏ setImmediate 回调

    - close callbacks : 执⾏ close 事件的 callback

# promise（。。）

Promise 是现代 Web 异步开发的重要组成部分，基本上目前所有的 Web 应用的异步开发手段都是通过 Promise 来实现的。

**概念**

所谓 Promise，就是一个容器对象，里面保存着某个未来才会结束的事件（异步事件）的结果。Promise 是一个构造函数，它有三个特点：

1.  Promise 有三个状态：pending（进行中）、fulfilled（成功）和 reject（失败），并且状态不受外部影响。
2.  状态一旦改变就无法修改，并且状态只能从 pending 到 fulfilled 或者是 pending 到 reject。
3.  Promise 一旦创建就会立即执行，不能中途取消。

**用法**

在 Promise 诞生之前，Web 应用中的异步开发主要采用的是回调函数的模式（详情可以参考 node.js 各个 API），回调函数的一大缺点就是，当我们的一个异步结果需要使用另外一个异步结果时，就会产生回调嵌套，一旦这样的嵌套多了，就会变成回调地狱，十分影响代码观感。

而 Promise 的诞生一定程度上解决了这个问题，因为 Promise 是采用链式调用的方式，并且在 Promise 返回的 Promise 对象中的 then、catch 等一系列方法都会返回一个新的 Promise 对象。

**then 方法**

当 Promise 实例创建成功后，可以执行其原型上的 then 方法。then 方法接受两个参数，分别是当前 Promise 的成功回调和失败回调，并且这两个函数会自动返回一个新的 Promise 对象。

then 方法的成功回调如果返回的是一个 Promise 对象，那么只有当这个 Promise 对象状态发生改变之后，才会执行下一个 then。

**catch 方法**

Promise 原型上还有一个 catch 方法，它会捕获在它链式之前的所有未被捕获的错误（一旦前面的错误被捕获，就不会执行）。

catch 只是捕获异常，catch 并不能终止当前 Promise 的链式调用。

同样的，catch 方法也会自动返回一个新的 Promise 对象，一旦显示返回一个 Promise，那么只有当这个 Promise 对象状态发生改变时，链式调用才会继续往下走。

**finally 方法**

在 ES8 中新加入的方法，此方法和 then、catch 不同，它不会跟踪 Promise 的状态，即不管 Promise 最终变成了什么状态，都会执行这个方法，同时 finally 不接收任何参数。

同样的，finally 并不是链式调用的终点，它也会自动返回一个新的 Promise 对象。

**Promise.all()** // 并发执行多个Promise，返回一个Promise，所有Promise都成功时返回成功结果，有一个失败则返回失败结

**Promise.allSettled()** // 并发执行多个Promise，返回一个Promise，所有Promise都成功或失败时返回成功或失败结果 

**Promise.any()** // 并发执行多个Promise，返回一个Promise，只要有一个Promise成功则返回成功结果，所有Promise都失败则返回失败结果 

**Promise.race()** // 并发执行多个Promise，返回一个Promise，只要有一个Promise成功或失败则返回成功或失败结果 

**Promise.resolve()** // 返回一个成功的Promise

**Promise.reject()** // 返回一个失败的Promise

# 普通函数/箭头函数/new

- 箭头函数

  - 无this，可从上层作用域继承

  - this指向不变，不会因为谁调用改变

  - 不能new构造对象

  - 无arguments

  - 无prototype

- new

  - 生成对象

  - this指向该对象

  - 执行构造函数

  - 返回该对象

  ```
  // 手写new
  const newInstance = (fn, ...args) => {
    const obj = Object.create(fn.prototype) // 创建一个新对象，继承构造函数的原型
    const res = fn.apply(obj, args) // 将构造函数的this指向新创建的对象，并传入参数
    return res instanceof Object ? res : obj // 如果构造函数返回的是一个对象，则返回该对象，否则返回新创建的对象
  }
  ```

  

# 深拷贝/浅拷贝

- 浅拷贝：拷贝对象，属性是引用类型，两个对象共享一块内存，修改一个对影响另一个.
  Object.assign(target, ...sources) 或  {...obj} 或 Array.slice()或[...arr]

- 深拷贝：会递归地复制原始对象的所有属性，生成是一个新对象

  ```javascript
  JSON.parse(JSON.stringify(obj)) 
  //或
  function deepCopy(obj,cache = new WeakMap()) { 
  	if (obj === null || typeof obj !== 'object') {return obj;} //obj为原始值，直接返回
    if (cache.has(obj)) return cache.get(obj); // ******处理循环引用
  	const copy = Array.isArray(obj) ? [] : {};    
    cache.set(obj, copy); // ******缓存当前对象
    for (const key in obj) {    
      if (obj.hasOwnProperty(key)) {    // 只拷贝自身属性   
        copy[key] = deepCopy(obj[key]); // 递归复制    
      }  
    }    
    return copy;}
  ```

  **边界状况**：建议用三方库lodash.cloneDeep
  1、基本数据类型：null，undefined，number，string，boolean直接返回
  2、对象，数组 需要递归拷贝
  3、循环引用，使用WeakMap 记录已处理的对象。

  ```
  function deepCopy(obj, cache = new WeakMap()) {
    if (typeof obj !== 'object' || obj === null) return obj;
    
    // 处理循环引用
    if (cache.has(obj)) return cache.get(obj);
    
    const copy = Array.isArray(obj) ? [] : {};
    cache.set(obj, copy); // 缓存当前对象
    
    for (const key in obj) {
      if (obj.hasOwnProperty(key)) {
        copy[key] = deepCopy(obj[key], cache); // 递归并传递缓存
      }
    }
    
    return copy;
  }
  
  // 测试循环引用
  const a = {};
  a.b = a; // 循环引用
  const copy = deepCopy(a);
  console.log(copy.b === copy); // 输出: true（正确处理循环引用）
  ```

  4、特殊对象：日期对象（Date）return new Date(obj.getTime());正则表达式（RegExp）return new RegExp(obj);Map/Set；Function
  5、不可枚举属性，Symbol
  6、原型链

# useStrict

1、禁止使用未声明变量，重复声明 

2、禁止删除变量 

3、this是undefined

4、只读属性不能赋值 

5、防止不安全才做 

6、严格解析

# 柯里化

将多参数函数转换为一系列单参数函数的技术，将f(a, b, c) 转换为 f(a)(b)(c) 

```javascript
function curry(fn) {  
	return function curried(...args) {    
		if (args.length >= fn.length) { // 参数够了，执行原函数      
      return fn(...args);    }
		else { // 参数不够，返回新函数继续收集      
			return function(...moreArgs) { return curried(...args, ...moreArgs); };    
    }  
  };
}
const add = (a, b, c) => a + b + c;
const curriedAdd = curry(add);
//curriedAdd(1)(2)(3)，curriedAdd(1, 2)(3)，curriedAdd(1)(2, 3)
```

# 继承

**原型链继承**

```
function Parent() {
  this.name = 'parent';
  this.colors = ['red', 'blue'];
}

Parent.prototype.say = function() {
  console.log('hello');
}

function Child() {}
Child.prototype = Object.create(Parent.prototype); // 直接使用父类实例作为子类原型
Child.prototype.constructor = Child;
```

**组合继承**

```
function Parent(name) {
  this.name = name;
  this.colors = ['red', 'blue'];
}

Parent.prototype.say = function() {
  console.log('hello');
}

function Child(name, age) {
  Parent.call(this, name); // 第一次调用父类构造函数
  this.age = age;
}

Child.prototype = new Parent(); // 第二次调用父类构造函数
Child.prototype.constructor = Child;
```

**寄生组合继承**

```
function Parent(name) {
  this.name = name;
  this.colors = ['red', 'blue'];
}

Parent.prototype.say = function() {
  console.log('hello');
}

function Child(name, age) {
  Parent.call(this, name); // 继承属性
  this.age = age;
}

// 继承原型
Child.prototype = Object.create(Parent.prototype);
Child.prototype.constructor = Child;

// 子类可以添加自己的方法
Child.prototype.play = function() {
  console.log('playing');
};
```

**类继承**

```
class Parent {
  constructor(name) {
    this.name = name;
    this.colors = ['red', 'blue'];
  }
  
  say() {
    console.log('hello');
  }
}

class Child extends Parent {
  constructor(name, age) {
    super(name); // 必须先调用super
    this.age = age;
  }
  
  play() {
    console.log('playing');
  }
}
```

# 数组操作类型常用方法

| **分类**        | **方法及示例**                                               |
| --------------- | ------------------------------------------------------------ |
| **创建**        | [], Array.of(num), Array.from(string或{ length: 3 }, (_, i) => i) |
| **访问**        | [], at(), indexOf(), includes(), find()                      |
| **修改**        | **push(), pop(), shift(), unshift(), splice()**   `array.splice(start, deleteCount, item1, item2, ...);` |
| **遍历**        | for, for (const item of arr)  ，arr.forEach((item, index, array) =>{}) |
| **转换**        | map(), filter(), 累加reduce(), 扁平flat(), flatMap()先 map 再 flat.       //[1, 2, 3].reduce((acc, curr) => acc + curr, 0);       nested.flat(Infinity).    ["Hello world", "Goodbye "].flatMap(s => s.split(' '))` |
| **查找 / 判断** | arr.indexOf()索引，arr.includes()返回true;<br/>every(), some()至少一个,arr.find(x => x > 25)第一个满足元素，arr.findIndex(x => x > 25)索引 |
| **排序 **       | **sort(), reverse()**                                        |
| **合并 / 分割** | concat(), slice(), 展开语法 [...arr]  例merged.slice(2, 5); // 从索引2到5（不包含5） |

# 对象操作

**`Object.keys(obj)`**：自身可枚举属性名

**```obj.hasOwnProperty(key)```**:判断对象属性

**`Object.getOwnPropertyNames(obj)`**:获取对象自身所有属性名

**`Object.defineProperty(obj, 'b', { value: 2, enumerable: false });`**:设置对象属性



# 遍历for

| **方法**       | **速度（大致排序）** | **可中断性**                                       | **适用数据结构**             |
| -------------- | -------------------- | -------------------------------------------------- | ---------------------------- |
| **for 循环**   | 最快                 | ✅ `break`（完全终止）和 `continue`（跳过当前迭代） | 数组                         |
| **for...of**   | 较快                 | ✅                                                  | 可迭代对象（数组、Set、Map） |
| **forEach**    | 中等                 | ❌return仅跳过当前回调，无法终止循环                | 数组                         |
| **map/filter** | 较慢（需创建新数组） | ❌                                                  | 数组                         |
| **for...in**   | 最慢（遍历原型链）   | ✅                                                  | 对象                         |

**Object.entries()**：返回 `[key, value]` 对的数组

**Object.keys()**：返回[key]数组

# 获取元素位置

```javascript
const element = document.getElementById('myElement');  //getElementsByClassName,querySelector
var rect = element.getBoundingClientRect();
top: rect.top + window.scrollY,
right: rect.right,
bottom: rect.bottom,
left: rect.left + window.scrollX
```

# 判断是否是子元素

```javascript
// a在b内部
const isChild = b !== a && b.contains(a); //true✅
const relationship = b.compareDocumentPosition(a); //16在
function isChildOf(a, b) {
  let current = a;
  while (current) {
    if (current === b) return true;
    current = current.parentElement;
  }
  return false;
}
const isChild = a.closest('#b') === b; // 假设 b 的 ID 是 'b'
```

# 水平垂直居中

![img](https://api2.mubu.com/v3/document_image/28886397_4bb484cd-aa3f-4f86-f132-db99265d8c14.png)

# flex

- 容器6个属性
  - flex-direction属性决定主轴的方向
  - flex-wrap 是否换行
  - flex-flow 是上面两个的缩写
  - justify-content属性定义了项目在主轴上的对齐方式。
  - align-items属性定义项目在交叉轴上如何对齐。
  - align-content属性定义了多根轴线的对齐方式。如果项目只有一根轴线，该属性不起作用。
- 项目的6个属性
  - order属性定义项目的排列顺序。数值越小，排列越靠前，默认为0。
  - flex-grow 放大比例 默认为0，即如果存在剩余空间，也不放大。
    - 如果所有项目的flex-grow属性都为1，则它们将等分剩余空间（如果有的话）。如果一个项目的flex-grow属性为2，其他项目都为1，则前者占据的剩余空间将比其他项多一倍。
  - flex-shrink 缩小比例 默认为1，即如果空间不足，该项目将缩小。
    - 如果所有项目的flex-shrink属性都为1，当空间不足时，都将等比例缩小。如果一个项目的flex-shrink属性为0，其他项目都为1，则空间不足时，前者不缩小
  - flex-basis 分配多余空间之前，项目占据的主轴空间.
    - 浏览器根据这个属性，计算主轴是否有多余空间。它的默认值为auto，即项目的本来大小。
  - flex 上面三个的缩写 默认值为0 1 auto。后两个属性可选。
    - 该属性有两个快捷值：auto (1 1 auto) 和 none (0 0 auto)。
  - align-self 允许单个项目有与其他项目不一样的对齐方式。可覆盖align-items属性。默认值为auto，表示继承父元素的align-items属性，如果没有父元素，则等同于stretch。

**flex: 1**

```
flex-grow: 1;    /* 允许元素增长以填充可用空间 */
flex-shrink: 1;  /* 允许元素缩小以适应容器 */
flex-basis: 0%;  /* 元素的初始大小为 0 */
```

# css 选择器的优先级

!important > 行内样式 > id选择器 > 类选择器 > 标签选择器 > 通配符选择器 > 继承 > 浏览器默认样式

| **选择器类型**   | **权重值** | **示例**                   |
| ---------------- | ---------- | -------------------------- |
| **内联样式**     | `1000`     | `<div style="color: red">` |
| **ID 选择器**    | `100`      | `#header`                  |
| **类选择器**     | `10`       | `.container`               |
| **属性选择器**   | `10`       | `[type="text"]`            |
| **伪类选择器**   | `10`       | `:hover`, `:nth-child(2)`  |
| **元素选择器**   | `1`        | `div`, `p`                 |
| **伪元素选择器** | `1`        | `::before`, `::first-line` |
| **通配符选择器** | `0`        | `*`                        |
| **继承的样式**   | `无权重`   | 由父元素继承的样式         |

多个结合使用：累加

相同：后定义的优先级高

# 行内标签、块内标签

**块标签：div p h1-h6 hr ul ol li dl dd dt form** 

​      ①支持宽高，自上而下排列

​      ②不受空格影响

​      ③一般用于其他标签的容器

​      ④默认宽度为100%（独占一行）。

**行内标签：span i a b strong em sub sup u label br font**

​       ①不支持宽高（宽高根据内容大小自动撑开），自左向右排列

​       ②受空格影响

​       ③不独占一行

**行内块标签：img  textarea  input**

​        ①支持宽高，自左向右排列

​        ②受空格影响

​        ③不独占一行

**标签之间的转换**

display：inline（转为行内元素）

​       inline-block（转为行内块元素）

​       block（转为块元素）

​       none（隐藏 不显示）

注意：当元素浮动（float）时会转化成行内块元素特点。

# **position属性值**

1. **static**（默认值）：正常文档流，`top`、`right`、`bottom`、`left` 和 `z-index` 属性无效。
2. **relative**：正常文档流，通过 `top`、`right`、`bottom`、`left` 调整位置，相对于其正常位置偏移。可设置 `z-index` 
3. **absolute**：脱离文档流，定位相对于最近的**已定位祖先元素**（relative`、`absolute`、`fixed` 或 `sticky），同2.
4. **fixed**：脱离文档流，定位相对于**浏览器视口**，同2。用于实现固定导航栏、悬浮按钮等。
5. **sticky**：正常文档流，滚动到特定位置时变为固定定位。必须有`top`、`right`、`bottom`、`left`。用于实现粘性标题、侧边栏

# 伪元素、伪类

| **对比维度**     | **伪元素**                                                   | **伪类**                                                     |
| ---------------- | ------------------------------------------------------------ | ------------------------------------------------------------ |
| **本质**         | 创建虚拟元素（文档树外）                                     | 描述元素状态 / 位置（文档树内）                              |
| **语法**         | 使用 **双冒号 `::`**（CSS3 规范）                            | 使用 **单冒号 `:`**                                          |
| **数量**         | 一个选择器中最多使用 **1 个伪元素**                          | 一个选择器中可叠加多个伪类                                   |
| **操作对象**     | 操作元素的**部分内容或虚拟内容**                             | 操作元素的**整体状态或位置**                                 |
| **是否生成内容** | 可生成新内容（如 `::before`/`::after`），必须设置 content 属性 | 不生成新内容，仅匹配状态                                     |
| **常见用途**     | - 清除浮动（`::after`） - 添加装饰性内容 - 操作文本首字母 / 行 | - 交互状态（`:hover`/`:focus`） - 结构伪类（`:nth-child`） - 动态状态（`:disabled`） |

# BFC

**BFC（Block Formatting Context）** 是 CSS 中一种独立的渲染区域，它规定了内部元素如何布局，以及与外部元素的交互规则。

解决常见的布局问题（如高度塌陷、外边距重叠等）。

**触发 BFC 的条件**

1. **浮动元素**：`float` 值为 `left`/`right`（非 `none`）。
2. **绝对定位元素**：`position` 值为 `absolute`/`fixed`。
3. **行内块元素**：`display` 值为 `inline-block`。
4. **表格相关元素**：`display` 值为 `table-cell`/`table-caption` 等。
5. **overflow 非默认值**：`overflow` 值为 `auto`/`scroll`/`hidden`（非 `visible`）。
6. **弹性 / 网格容器**：`display` 值为 `flex`/`grid` 及其衍生值的直接子元素。

# **盒模型**

**标准盒模型**

- width就是content

**怪异盒模型（IE 盒模型）**

- width=content+padding+bording

- 适合固定宽高的布局（如响应式设计）

- ```
  box-sizing: border-box
  ```

# type和interface

| **特性**            | **`interface`** | **`type`**                 |
| ------------------- | --------------- | -------------------------- |
| 重复定义合并        | ✅（自动合并）   | ❌（报错）                  |
| 定义基本类型        | ❌               | ✅（如 `type ID = string`） |
| 定义联合 / 交叉类型 | ❌               | ✅（如 `type A = B & C`）   |
| 类实现              | ✅               | 仅支持对象类型的 type      |
| 扩展方式            | `extends`       | 交叉类型 `&`               |
| 映射类型 / 条件类型 | ❌               | ✅                          |

# any和unknow

any：任何类型，不推荐

unknow：any的安全写法，使用前先校验类型

# TCP和UDP

| 特性         | TCP                          | UDP                         |
| ------------ | ---------------------------- | --------------------------- |
| **连接性**   | 面向连接（三次握手）         | 无连接（直接发送）          |
| **可靠性**   | 可靠（确认机制、重传、排序） | 不可靠（可能丢包、乱序）    |
| **传输效率** | 低（头部开销 20 字节）       | 高（头部开销 8 字节）       |
| **传输方式** | 字节流（无边界）             | 数据报（有边界，不拆分）    |
| **拥塞控制** | 有（慢启动、拥塞避免）       | 无（可能导致网络拥塞）      |
| **应用场景** | HTTP、SMTP、FTP、数据库      | DNS、视频流、实时游戏、直播 |
