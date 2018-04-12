```
<div id='example-3'>
  <input type="checkbox" id="jack" value="Jack" v-model="checkedNames">
  <label for="jack">Jack</label>
  <input type="checkbox" id="john" value="John" v-model="checkedNames">
  <label for="john">John</label>
  <input type="checkbox" id="mike" value="Mike" v-model="checkedNames">
  <label for="mike">Mike</label>
  <br>
  <span>Checked names: {{ checkedNames }}</span>
</div>


new Vue({
  el: '#example-3',
  data: {
    checkedNames: []
  }
})


 Jack  John  Mike 
Checked names: []
```

```
<ul>
  <li
    v-for="(item, index) in data"
    :class="{'active' : index == activeIndex}"
    :key="index"
    v-model="checkedNames"
  >
    <input class="checkbox" type="checkbox" :id="index" v-model="checkedNames" :value="item.value" />
    <label :for="index">
      <p>{{item.nickname}}</p>
    </label>
  </li>
</ul>
```
