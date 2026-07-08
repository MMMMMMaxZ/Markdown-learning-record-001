# testMPE

<div id="my-board" class="jxgbox" style="width:600px; height:400px; margin: 0 auto;"></div>

<script>
    // 等待 DOM 加载完成后初始化画板
    document.addEventListener("DOMContentLoaded", function() {
        // 使用上面 <div> 的 id 来初始化画板
        var board = JXG.JSXGraph.initBoard('my-board', {
            boundingbox: [-5, 5, 5, -5],  // [xmin, ymax, xmax, ymin]
            axis: true,                   // 显示坐标轴
            showCopyright: false          // 隐藏右下角版权信息（可选）
        });

        // 画一个函数图像：y = x^2
        board.create('functiongraph', [function(x) { return x * x; }], {
            strokeColor: 'blue',
            strokeWidth: 2
        });

        // 画一个点
        board.create('point', [2, 4], { name: 'P', size: 4, color: 'red' });
    });
</script>
