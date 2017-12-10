<template>
  <footer class="footer">
      <ul>
          <li v-for="lis in ul">{{lis.li}}</li>
      </ul>
      <p>
          Copyright&nbsp;&copy;&nbsp;{{author}} - 2017 All rights reserved
      </p>
  </footer>
</template>

<script>
export default {
  name: 'footerDiv',
  data(){
      return {
          ul: [
              {li: '琉璃之金'},
              {li: '朦胧之森'},
              {li: '飘渺之涛'},
              {li: '逍遥之火'},
              {li: '璀璨之沙'},
          ]
      }
  },
  computed: {
      author(){
          return this.$store.state.author
      }
  }
}
</script>

<style>
.footer{
    position: absolute;
    width: 100%;
    bottom: 0;
}
.footer ul li{
    list-style: none;
    display: inline-block;
    width: 20%;
}
.footer p{
    text-align: center;
}
</style>
