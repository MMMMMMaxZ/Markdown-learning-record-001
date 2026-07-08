# JSX_test1

> 目标：
> 测试简单样例，掌握基本坐标图渲染方法
> 只能使用原本的Markdown渲染才看得到，哎

## 测试样例

```jsxgraph
// 1. 初始化画板，使用 containerId 作为容器
var board = JXG.JSXGraph.initBoard(containerId, {
    boundingbox: [-5, 5, 5, -5], // 设置坐标范围: [xmin, ymax, xmax, ymin]
    axis: true,                  // 显示坐标轴
    showCopyright: false
});

// 2. 添加几何元素
// 创建一个点，并命名为 A
var p1 = board.create('point', [-2, 2], { name: 'A', size: 4 });
// 创建另一个点，命名为 B
var p2 = board.create('point', [3, -1], { name: 'B', size: 4 });
// 用这两个点画一条蓝色的线
var line = board.create('line', [p1, p2], { strokeColor: 'blue' });
```

只要你保存文件并打开 Markdown 预览，这段代码就会自动渲染成可拖拽、缩放的可交互坐标图[citation:1]。

### 🗺️ 学习教程与进阶资源

掌握了基本用法后，可以参考以下资源深入学习：

- **JSXGraph 官方起步指南**：这是学习 JSXGraph 核心概念和 API 的最佳起点，文档里有很多**函数绘图、几何图形构造**的详细示例和可运行的 HTML 模板[citation:2]。
- **JSXGraph 初学者工作坊**：这是官方会议的工作坊材料，手把手教你从零开始，在 VS Code 里创建第一个 JSXGraph 项目，包含了创建**点、线、圆、函数图像以及添加交互滑块**的完整代码[citation:8]。它是学习路径的一个很棒的中文补充。
- **JSXGraph 官方文档与示例库**：JSXGraph 官网的文档页面汇总了**API 参考**和**大量交互式示例**，是遇到具体绘图问题时查阅的宝典[citation:5]。

### 💡 补充：扩展的高级配置

这个扩展还提供了一些便捷的进阶功能[citation:1]：

- **全局自定义函数**：你可以在 VS Code 的设置中搜索 `markdown-jsxgraph.customGlobalFunctions`，添加自己的 JavaScript 辅助函数，在所有 JSXGraph 代码块中复用。
- **内置工具函数**：扩展默认内置了 `__jxg` 开头的工具函数，可以用于创建美观的**矩阵渲染**、**动画播放控制**和**高性能动画循环**。
