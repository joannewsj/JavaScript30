## 15 Local Storage

[Demo](https://joannewsj.github.io/JavaScript30/15%20-%20LocalStorage/)

```Javascript
addItems.addEventListener('submit', addItem);

function addItem(e){
    console.log('hello');
}
```

在input填写后submit 会发现整个页面会刷新 因为这是 `submit` 的default行为
用 `e.preventDefault()` 来防止刷新

```Javascript
function addItem(e){
    e.preventDefault();
    console.log('hello');
}
```

取input的值 再加入items array里
```Javascript
const text = (this.querySelector('[name=item]')).value;
const item = {
    text: text, //也可以只写[text,]
    done: false
}
items.push(item);
this.reset(); //清除input
```

把数据放进HTML和localStorage
```Javascript
function addItem(e){
    populateList(items, itemsList);
}

function populateList(plates = [], platesList){
    platesList.innerHTML = plates.map((plate, i) => {
        return `
            <li>
                <input type="checkbox" data-index=${i} id="item${i}" ${plate.done ? 'checked' : ''}/>
                <label for="item${i}">${plate.text}</label>
            </li>
        `;
    }).join('');
}
```
