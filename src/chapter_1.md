# Learn Svelte Quickly

2016 年创建, 为了解决前端框架在运行性能上的瓶颈, 主要优势在于它在构建阶段就进行了优化，将模板和逻辑转换为简单的DOM操作，减少了运行时的开销。

- 无虚拟 DOM
- 将复杂性从运行时转移到编译时

学习前提：

- 熟悉最基本的前端知识(HTML、CSS、JavaScript)和 Node
- 使用过一些响应式框架（Vue、React等）开发过 WebApp 项目

两大部分：

### 1. Svelte 基础

- [简洁的组件系统](./component.md)
- Reactive Statements 响应式系统
  - Reactive Declarations
  - Reactive Blocks
- 编译过程

关于性能优化的细节:
- 模板内联, 运行时无需模板解析步骤
- 计算属性缓存, 避免重复计算
- 事件处理优化
- 代码分割和懒加载,按需加载组件

进阶的一些内容点:
- Store: Svelte Store是一种共享状态管理的机制，可以跨组件传递和更新数据。它简化了组件间的通信，同时保持了响应式更新。
- Actions: Actions是在组件挂载时运行的函数，可以用于处理DOM操作、事件监听和其他复杂逻辑。
- Slots: Svelte的插槽机制允许在父组件中插入子组件的内容，实现内容分发。
- Custom Elements: Svelte组件可以作为自定义元素使用，与其他库和框架（如React、Angular）集成。

### 2. 框架体系


### 3. 前端工程

- HMR 实时重载和热模块替换
- TypeScript
- Vite & Snowpack
- VSCode Plugin

### 4. 学习案例


### 额外：Svelte 的一些变化与前瞻

Svelte 5 Preview: https://svelte.dev/blog/svelte-5-release-candidate
