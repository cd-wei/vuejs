<template>
  <div>
    <p>this is a simple component</p>
    <slot name="nav" v-for="nav in navs" :text="nav.text"></slot>
  </div>
</template>

<script>
export default {
  name: 'simple',
  data(){
      return {
        navs: []
      }
  }
}
</script>
