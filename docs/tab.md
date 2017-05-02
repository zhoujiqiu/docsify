# Tab

##### 选项卡，点击 tab 会切换显示的页面

#### 引入

``` bash
import TTabbar from 'toon-ui/lib/components/tabbar'

components: {
  TTabbar
}

```
#### template
``` html
 <t-tabbar v-bind:tabs='tabs' v-on:tabchange="tabChange"></t-tabbar>
```

#### javascript
``` js
methods: {
  tabChange: function (index) {
    let j = parseInt(index) // 注意，需转化为整数
    this.tabs.isSelectCon.splice(j, 1, '我可以是post请求回来的数据哟'+j)
  }
}
```

初始化参数配置
``` bash
tabs:{
  isSelect: 0, // 第几个选中，默认不传0开始计
  isSelectCon: ['我初始化的年度内容', '我初始化的月度内容', '我初始化的季度内容'], // 选中的内容数组，无内容为空
  tabList: ['年度', '月度', '季度'] // tab的title值数组，默认无值
}
```

#### 演示
[点击查看DEMO](https://zhoujiqiu.github.io/toon-ui/dist/#!/demo/tab)

