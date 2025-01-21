# Component: 简洁的组件系统

在 Svelte 中, 应用程序是由一个或多个组件有机组合而成:
- 组件是一个可重复使用的独立代码块( .svelte 文件);
- 由 HTML, CSS 以及 JavaScript 编写;
- 组件会被编译小巧且高效的 JavaScript 模块在浏览器中运行;

组件代码足够简单, 如果你熟悉前端基础知识, 理解起来没有什么难度.

App.svelte 组件内容示例说明:

```javascript
<div class="content">
  <img {src} alt="{name} Logo">
  <h3>了解 {name.toUpperCase()} 组件基础</h3>
  <p>{@html desc}</p>
  
  <Nested />
</div>

<script>
  // 引入子组件
  import Nested from './Nested.svelte';

  let name = "Svelte";
  let desc = `应用程序是由一个或多个<strong> [组件] </strong>有机组合而成`;
  let src = "https://s3.cdnjson.com/images/2024/11/19/component.png";
</script>

<!-- 样式规则仅在组件内生效 -->
<style> 
  .content { text-align: center; }
  img { width: 100%; }
</style>
```
引入的子组件内容说明: 

```javascript
<p>以下内容自于一个嵌入组件.</p>

<script>
  let { time } = $props();
</script>
```

通过这两个文件你就可以学习到:
- 基本的组件模板语法, 定义变量, 展示以及 HTML Element 的属性赋值等等;
- 如何引入子组件, 并在组件之间传输数据;


