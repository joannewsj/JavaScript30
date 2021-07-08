## 02 JS and CSS Clock

[Demo](https://joannewsj.github.io/JavaScript30/02%20-%20JS%20and%20CSS%20Clock/)

1. `transform-origin` 改变转换元素的位置  
`transform-origin: x-axis y-axis z-axis;`  
默认值是 `50% 50% 0`  
2. `transform` 对元素进行 `rotate`, `scale` `translate`, `skew`  
3. `transition` 有4个属性 `transition-property`, `transition-duration`, `transition-timing-function`, `transition-delay`  
一定要设置`transition-duration`，否则时长为0  
4. `transition-timing-function` 规定过渡效果的速度曲线  
6个属性:  
`linear` 等于 `cubic-bezier(0, 0, 1, 1)`  
`ease` 等于 `cubic-bezier(0.25, 0.1, 0.25, 0.1)`  
`ease-in` 等于 `cubic-bezier(0.42, 0, 1, 1)`  
`ease-out` 等于 `cubic-bezier(0, 0, 0.58, 1)`  
`ease-in-out` 等于 `cubic-bezier(0.42, 0, 0.58, 1)`  
`cubic-bezier(n,n,n,n)` 自己定义0-1的值
