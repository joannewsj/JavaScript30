## 01 JavaScript Drum Kit

1. [JavaScript Keycodes](https://keycode.info/)
2. `data-key` 是自定义属性，在网上是搜寻不到的
3. 监听keydown event
`window.addEventListener('keydown', function(){});`
**keydown vs keypress**
keydown: 任何键盘按键按下都可以取得对应得键盘代码，不区分大小写
keypress: 只会针对可以输出文字符号的按键有效，大小写会取得不同的keycode
4. 播放audio `audio.play()`
重置audio播放时间 `audio.currentTime = 0`
5. 添加和移除class name `selector.classList.add('playing')` `key.classList.remove('playing')`
6. transition结束后会执行transitionend事件
```
const keys = document.querySelectorAll('.key');
keys.forEach(key => key.addEventListener('transitionend', removeTransition));
```
