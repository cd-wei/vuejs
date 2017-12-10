<template>
  <div id="firstcomponent">
      <h1>标题</h1>
      <a>作者：{{ author }} </a>
  </div>
  </template>

<script>
export default{
  data () {
    return {
      author: 'cdw'
    }
  }
}
</script>

<style>
</style>
