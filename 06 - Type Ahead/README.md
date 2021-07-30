## 06 Type Ahead

[Demo](https://joannewsj.github.io/JavaScript30/06%20-%20Type%20Ahead/)

1. 基本`fetch`请求
``` javascript
fetch('http://example.com/movies.json')
    .then(response => response.json())
    .then(data => console.log(data));
```

2. Regular Expression
``` javascript
const regex = new RegExp(wordToMatch, 'gi');
```
`g`表示全局搜索，`i`表示忽略大小写  

[学习regex](https://github.com/ziishaned/learn-regex/blob/master/translations/README-cn.md)  
[线上练习regex](https://regex101.com/)
