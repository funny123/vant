<template>
  <div class="hello">
    <!-- <h1>{{ msg }}</h1> -->
    <div class="navbar">
      <van-nav-bar
  title="标题"
  left-text="返回"
  right-text="按钮"
  left-arrow
  @click-left="onClickLeft"
  @click-right="onClickRight"
/>
 </div>
 <div class="layout">
  <van-card
  num="2"
  tag="标签"
  price="2.00"
  desc="描述信息"  
  title="商品标题"
  :thumb="imageURL"
  origin-price="10.00"
>

  <div slot="footer">
    <van-button size="mini">按钮</van-button>
    <van-button size="mini">按钮</van-button>
  </div>
</van-card>
 </div>
  <div class="tabbar">
    <van-tabbar v-model="active" @change="onChange">
  <van-tabbar-item icon="shop">标签</van-tabbar-item>
  <van-tabbar-item icon="chat" dot>标签</van-tabbar-item>
  <van-tabbar-item icon="records" info="5">标签</van-tabbar-item>
  <van-tabbar-item icon="gold-coin" info="20">标签</van-tabbar-item>
</van-tabbar>
  </div>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  props: {
    msg: String
  },
  data() {
    return {
      active: 0,
      imageURL:'https://img.yzcdn.cn/2.jpg',
      list: [],
    };
  },
  methods: {
    onLoad() {
          this.list.length=10;
    },
    onChange(val) {
      //  Toast('123213')
      console.log("tag", val);
    },
    onClickLeft() {
      console.log("返回");
    },
    onClickRight() {
      console.log("按钮");
    },
    
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
