## 18 Adding Up Times with Reduce

[Demo](https://joannewsj.github.io/JavaScript30/18%20-%20Adding%20Up%20Times%20with%20Reduce/)

1. 使用 `document.querySelectorAll('')`，取到的内容是 NodeList 不是 array

2. 把NodeList换成Array有2个方法：
   - `const nodeArray = [...document.querySelectorAll("div")]`
   - `Array.from(document.querySelectorAll("div"))`  

3. `parseFloat`
    ``` Javascript
    timeNodes.map(function (str){
        return parseFloat(str);
    })
    ```
    可以缩短成
    ``` Javascript
    timeNodes.map(parseFloat);
    ```
