## 11 Custom Video Player

1. 获取元素
```
const player = document.querySelector('.player');
const video = player.querySelector('.viewer');
const progress = player.querySelector('.progress');
const progressBar = player.querySelector('.progress__filled');
const toggle = player.querySelector('.toggle');
const skipButtons = player.querySelectorAll('[data-skip]');
const ranges = player.querySelectorAll('.player__slider');
```

2. 播放/暂停
`video` 可以用 `paused` 来判断影片是否在播放
```
function togglePlay(){
    const method = video.paused ? 'play' : 'pause';
    video[method]();
}
video.addEventListener('click', togglePlay);
toggle.addEventListener('click', togglePlay);
```

3. 换图标
虽然可以用 `togglePlay` 切换图标，但是user可以用第三方来控制
一样用 `paused` 来判断影片是否在播放
```
function updateButton(){
    const icon = video.paused ? '►' : '❚ ❚';
    toggle.textContent = icon;
}
video.addEventListener('play', updateButton);
video.addEventListener('pause', updateButton);
```

4. fast forward/fast backward
在HTML中有`data-skip`属性 可以用`dataset`来获取
```
function skip(){
    video.currentTime += parseFloat(this.dataset.skip);
}
skipButtons.forEach(button => button.addEventListener('click', skip));
```

5. 音量和播放速度
```
function handleRangeUpdate(){
    video[this.name] = this.value;
}
ranges.forEach(range => range.addEventListener('change', handleRangeUpdate));
ranges.forEach(range => range.addEventListener('mousemove', handleRangeUpdate));
```

6. 进度条操作
```
function handleProgress(){
    const percent = (video.currentTime / video.duration) * 100;
    progressBar.style.flexBasis = `${percent}%`;
}
video.addEventListener('timeupdate', handleProgress);
```
根据点击位子设置
```
function scrub(e){
    const scrubTime = (e.offsetX / progress.offsetWidth) * video.duration;
    video.currentTime = scrubTime;
}
let mousedown = false;
progress.addEventListener('click', scrub);
progress.addEventListener('mousemove', (e) => mousedown && scrub(e));
progress.addEventListener('mousedown', () => mousedown = true);
progress.addEventListener('mouseup', () => mousedown = false);
```
