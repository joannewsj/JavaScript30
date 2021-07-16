## 03 CSS Variables
[Demo](https://joannewsj.github.io/JavaScript30/03%20-%20CSS%20Variables/)  


1. `:root` 和 `var()`

``` Javascript
:root{
    --base: #FFC600;
}
img{
    background: var(--base);
}
```
2. NodeList 和 Array 的差别  
Inspect ``__proto__`` NodeList有 `forEach()`, `item()`, `keys()`，Array有 `map()`, `pop()`  

3. `dataset`  
用`dataset`来访问自定义属性(`data-`)  

4. 用 Javascript 改变 CSS  
`document.documentElement.style.setProperty('--base', '#fff');`  
document.documentElement 会回传目前文件(document)中的根元素(element), eg: HTML中的元素  
CSS內的 :root 对应的就是元素，所以要改变 :root 內设定的元素值就是使用document.documentElement
