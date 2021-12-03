## 19 Webcam Fun

[Demo](https://joannewsj.github.io/JavaScript30/19%20-%20Webcam%20Fun/)

1. 需要建立一个localhost服务器  
    `npm install` 安装  
    `npm start` 启动  
    访问 `http://localhost:3000/`

2. `navigator.mediaDevices.getUserNedia()` 会获取camera的权限，然后返回promise

3. `window.URL.createObjectURL(localMediaStream);` 已经depreceated  
    现在使用 `video.srcObject = localMediaStream;`

4. `canplay`  
    `video.addEventListener('canplay', paintToCanvas);`  
    当可以播放影片的时候触发事件

5. `canvas.toDataURL('image/jpeg')` 把图片转成base64

6. `let pixels = ctx.getImageData(0, 0, width, height)`  
    pixels会返回array 记录每个pixel的rgba  
    ``` Javascript
    console.log(pixels);
    // [1st pixel's R, 1st pixel's G, 1st pixel's B, 1st pixel's A, 2nd pixel's R, 2nd pixel's G, ......]
    ```

7. 先拿pixels出来 换effect 再放进去  
    ``` Javascript
    let pixels = ctx.getImageData(0, 0, width, height);
    pixels = redEffect(pixels);
    ctx.putImageData(pixels, 0, 0);
    ```
