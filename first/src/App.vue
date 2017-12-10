<template>
  <div id="app">
    <HeaderDiv :logo="logoMsg"></HeaderDiv>
    <Simple :navs="navs">
      <template slot="nav" slot-scope="props">
        <li>{{ props.text }}</li>
      </template>
    </Simple>
    <div class="login">
      <LoginDiv @transferUser="getUser"></LoginDiv>
      <p>用户名为：{{user}}</p>
    </div>  
    <FooterDiv></FooterDiv>
  </div>
</template>

<script>
import HeaderDiv from './components/header'
import LoginDiv from './components/login'
import FooterDiv from './components/footer'
import Simple from './components/simple'
export default {
  name: 'app',
  data(){
    return {
      logoMsg: 'cdw',
      user: '',
      navs: [
        {text: 'hello'},
        {text: 'man'},
        {text: 'fuck'}
      ]
    }
  },
  methods: {
    getUser(msg){
      this.user = msg
    },
  },
  components: {
    HeaderDiv,
    LoginDiv,
    FooterDiv,
    Simple
  }
}
</script>

<style scoped>
  .login{
    width: 400px;
    height: 100px;
    border: 1px solid black;
    margin: 0 auto;
  }
</style>
