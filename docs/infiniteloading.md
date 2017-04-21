# InfiniteLoading

##### 底部无限加载

#### 引入

``` bash
import InfiniteLoading from 'toon-ui/lib/components/infiniteloading'
export default {
  components: {
    InfiniteLoading
  }
}
```

#### 例子
Template
``` html
<div>
  <p v-for="item in list">
    Line:
    <span v-text="item"></span>
  </p>
  <infinite-loading :on-infinite="onInfinite" ref="infiniteLoading">
      <span slot="no-more">
        没有更多数据 :(
      </span>
  </infinite-loading>
</div>
```

Script
``` js
import InfiniteLoading from 'vue-infinite-loading'

export default {
  data() {
    return {
      list: []
    }
  },
  methods: {
    onInfinite() {
      setTimeout(() => {
        const temp = []
        for (let i = this.list.length + 1; i <= this.list.length + 20; i++) {
          temp.push(i)
        }
        this.list = this.list.concat(temp)
        this.$refs.infiniteLoading.$emit('$InfiniteLoading:loaded')
      }, 1000)
    }
  },
  components: {
    InfiniteLoading
  }
}
```


#### 演示
[点击查看DEMO](https://zhoujiqiu.github.io/toon-ui/dist/#/demos/infiniteloading)

