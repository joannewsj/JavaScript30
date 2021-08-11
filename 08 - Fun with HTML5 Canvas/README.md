## 08 Fun with HTML5 Canvas

Canvas用于绘制形状，文本，图像和其他对象
首先必须有HTML`<canvas>`元素才能使用
``` Javascript
    <canvas id="draw" width="800" height="800"></canvas>
    const canvas = document.querySelector('#draw');
    const ctx = canvas.getContext('2d');
```

设定canvas的大小
``` Javascript
    canvas.width = window.innerWidth;
    canvas.height = window.innerHeight;
```

`ctx.strokeStyle = '#BADA55'; `  图形边线的颜色和样式
`ctx.lineJoin = 'round'; `  两线相交拐点的类型 (round / bevel / miter(默认))
`ctx.lineCap = 'round'; `  线末端的类型 (butt(默认) / round / square)
`ctx.lineWidth = 100; `  线的宽度
`ctx.beginPath(); `  开始一个新的路径
`ctx.moveTo(lastX, lastY); `  路径的起点
`ctx.lineTo(e.offsetX, e.offsetY); `  路径的终点
`ctx.stroke(); `  使用当前的样式绘制路径

HSL [https://mothereffinghsl.com/](https://mothereffinghsl.com/)
Hue 色相
Saturation 饱和度 - 越高色彩越纯，低则逐渐变灰
Lightness 亮度
