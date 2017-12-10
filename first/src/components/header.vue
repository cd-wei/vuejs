<template>
  <header class="header">
      <div id="logo">
          {{logo}}
          <input placeholder="请输入内容" v-model="inputTxt" />
          <button slot="append" @click="setAuthor">修改</button>
      </div>
      <ul class="nav">
          <li v-for="nav in navs">{{nav.li}}</li>
      </ul>
  </header>
</template>
<script>
export default {
  name: 'headerDiv',
  data(){
      return {
          inputTxt: '',
          navs: [
              {li: '主页'},
              {li: '日志'},
              {li: '说说'},
              {li: '留言'},
              {li: '相册'}
          ]
      }
  },
  props: ['logo'],
  methods: {
      setAuthor: function(){
          this.$store.state.author = this.inputTxt
      }
  }
}
</script>
<style>
.header{
    background-color: gray;
    width: 100%;
    height: 50px;
}
#logo{
    float: left;
    height: 50px;
    line-height: 50px;
    margin-left: 5%;
    text-align: center;
    vertical-align: middle;
}
.nav{
    float: right;
    width: 50%;
    height: 50px;
    /* margin-right: 2%; */
}
.nav li{
    float: right;
    width: 10%;
    display: inline-block;
    list-style: none;
}
</style>
