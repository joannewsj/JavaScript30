## 14 JavaScript References VS Copying

[Demo](https://joannewsj.github.io/JavaScript30/14%20-%20JavaScript%20References%20VS%20Copying/)

```
let age = 100;
let age2 = age;
console.log(age, age2); // 100 100
age = 200;
console.log(age, age2); // 200 100
```

```
let name = 'Wes';
let name2 = name;
console.log(name, name2); // Wes Wes
name = 'Wesley';
console.log(name, name2); // Wesley Wes
```

```
const players = ['Wes', 'Sarah', 'Ryan', 'Poppy'];
const team = players;
console.log(players, team);
// ['Wes', 'Sarah', 'Ryan', 'Poppy'] ['Wes', 'Sarah', 'Ryan', 'Poppy']
team[3] = 'Lux';
console.log(players, team);
// ['Wes', 'Sarah', 'Ryan', 'Lux'] ['Wes', 'Sarah', 'Ryan', 'Lux']
```
这里会发现原本的string和number不会被改 反而原本的array被修改了
这是因为array会reference回去 所以我们需要copy
有四种方法：

```
const team2 = players.slice();`
const team3 = [].concat(players);
const team4 = [...players];
const team5 = Array.from(players);
```

object也和array一样 会reference回原本的object
```
const person = {
    name: 'Wes Bos',
    age: 80
};
const captain = person;
captain.number = 99;
console.log(person);
// {name: 'Wes Bos', age: 80, number: 99}
```
所以我们也需要copy
`Object.assign(target, ...sources)`
```
const cap2 = Object.assign({}, person, {number: 99, age: 12});
```
也可以用JSON转换
```
const wes = {
    name: 'Wes',
    age: 100,
    social: {
        twitter: '@wesbos',
        facebook: 'wesbos.developer'
    }
};
const dev = Object.assign({}, wes);
const dev2 = JSON.parse(JSON.stringify(wes));
```
