# docsify使用指南


## 渲染mermaind图显示[object Promise]

```html
<link rel="stylesheet" href="//cdn.jsdelivr.net/npm/mermaid/dist/mermaid.min.css">
<script src="//cdn.jsdelivr.net/npm/mermaid/dist/mermaid.min.js"></script>

<!-- 更换mermaind为9.3.0版本 -->
<script src="//cdn.jsdelivr.net/npm/mermaid@9.3.0/dist/mermaid.min.js"></script>
```
问题原因是官方文档中是按上述方式引入的mermaid最新版，而这个最新版渲染svg是异步的，所以导致页面中显示结果为`[object Promise]`。

?> _解决办法_
1. 更换mermaid为V9.3.0版本
2. 使用这个插件[mermaid-docsify](https://github.com/Leward/mermaid-docsify)

> [参考这个ISSUE](https://github.com/docsifyjs/docsify/pull/2490#pullrequestreview-2242989881)
> 番外：上面这个ISSUE实际上在24年8月已经对这个问题进行了探讨并提了PR也merge了,同时把文档中默认的`mermaid`版本切换到了V9.3.0版本。但是由于docsify一直没发布新版本，所以我们根据官方文档来集成mermaind就出现了上面那个问题。

!> docsify目前发布的最新版还是V4.13.1,这个版本还是23年6月24日发布，当时mermaid可能还没加上异步渲染所以是正常的。主要是这个工具发布周期太长了，期间mermaid升级了异步渲染，所以出现了上面的兼容性问题。

> 参考：https://zhuanlan.zhihu.com/p/715754435

## docsify部署

## GA统计
1. Google GA
2. matomo开源，前身为pwiki
3. [github pages](https://docs.github.com/zh/pages/quickstart)