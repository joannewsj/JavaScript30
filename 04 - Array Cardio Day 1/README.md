## 04 Array Cardio Day 1  
[Demo](https://joannewsj.github.io/JavaScript30/04%20-%20Array%20Cardio%20Day%201/)  

1. `filter` 过滤操作
    ``` Javascript
    const fifteen = inventors.filter(inventor => (inventor.year >= 1500 && inventor.year < 1600));
    ```

2. `map` 把array进行处理后，返回新的array
    ``` Javascript
    const name = inventors.map(inventor => (inventor.first + ' ' +  inventor.last));
    ```

3. `sort`
    ``` Javascript
    const age = inventors.sort((a, b) => a.year > b.year ? 1 : -1);
    ```

4. `reduce`
    ``` Javascript
    array.reduce(function(total, currentValue, index, arr), initialValue)
    ```
    更多使用reduce方法  
    [JavaScript中的reduce()的5个用例](https://www.huaweicloud.com/articles/3440fed1f55ae5f5fc9f423cd9e77de2.html)  
    [如何使用 JavaScript reduce 方法](https://chinese.freecodecamp.org/news/the-ultimate-guide-to-javascript-array-methods-reduce/)
