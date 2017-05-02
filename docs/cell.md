# Cell

##### 列表信息展示

#### 引入

``` js
import tCell from 'toon-ui/lib/components/tcell'

export default {
  components: {
    tCell
  }
}
```
#### 例子
基本用法
``` html
<t-cell title="标题文字"></t-cell>
<t-cell title="标题文字" value="说明文字"></t-cell>
```
带链接 `is-link`
``` html
<t-cell title="标题文字" is-link value="带链接"></t-cell>
```

带 `icon`
``` html
<t-cell title="标题文字" icon="more" value="带 icon"></t-cell>
```

自定义内容
``` html
<t-cell title="标题文字" is-link>
  <span style="color: green">这里是元素</span>
</t-cell>
```

#### 演示
[点击查看DEMO](https://zhoujiqiu.github.io/toon-ui/dist/#/demos/tcell)

