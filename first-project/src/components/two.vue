<template>
  <div @click="commit">
      <p>这是two组件<button @click="commit">给one组件发送信息</button></p>
      <p>{{ message }}</p>
  </div>
</template>

<script type="text/javascript">
import { bus } from "./bus";
export default {
  name: 'two',
  data(){
      return {
          message: ''
      }
  },
  methods: {
      commit(){
          bus.$emit('backMsg',{
              msg: '这条信息来自于two'
          })
      }
  },
  mounted(){
      bus.$on('sendMsg',(data) => {
          this.message = data.msg;
      })
  }
}
</script>
