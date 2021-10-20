## 09 Dev Tools Domination

1. 添加breakpoint
Inspect > Elements > 选择 `<p>` > 右键 > Break on > Attributes modifications
添加breakpoint后，它的属性改变时，会自动定位到 Sources

2. 修改style
`%c` - `console.log('%c I am a great text', 'font-size:40px;');`

3. warning
`console.warn` - `console.warn('OH NOOO');`

4. error
`console.error` - `console.error('Shit!);`

5. info
`console.info` - `console.info('Crocodiles eat 3-4 people per year');`

6. assert
false的时候才会出现第二个参数的内容
`console.assert` - `console.assert(1 === 1, 'That is wrong!')`
```
const p = document.querySelector('p');
console.assert(p.classList.contains('ouch'), 'That is wrong!');
```

7. clear
清除console内容 `console.clear`

8. DOM元素
`console.log` 会打印HTML标签 `console.dir` 会打印元素的属性列表
```
const p = document.querySelector('p');
console.log(p);
console.dir(p);
```

9. group
```
const dogs = [{ name: 'Snickers', age: 2 }, { name: 'hugo', age: 8 }];
dogs.forEach(dog =>{
    console.group(`${dog.name}`);
    console.log(`This is ${dog.name}`);
    console.log(`${dog.name} is ${dog.age} years old`);
    console.log(`${dog.name} is ${dog.age * 7} dog years old`);
    console.groupEnd(`${dog.name}`);
});
```
如果太乱想要收起列表 可以用 `console.groupCollapsed`
`console.groupCollapsed(`${dog.name}`);`

10. count
计算使用 `console.count` 出现多少次

11. timing
计算获取data需要多少时间
```
console.time('fetching data');
fetch('https://api.github.com/users/wesbos')
    .then(data => data.json())
    .then(data => {
        console.timeEnd('fetching data');
        console.log(data);
    })
```
