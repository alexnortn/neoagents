<template lang="pug">
  #app
    img(src="./assets/logo.png")
    hello
</template>


<script>
import Hello from './components/Hello'
// require THREE from 'three'
var THREE = require('three')

console.log(THREE)

export default {
  name: 'app',
  components: {
    Hello
  }
}
</script>


<style lang="stylus">
#app
  font-family 'Avenir', Helvetica, Arial, sans-serif
  font-smoothing antialiased
  
  text-align center
  
  color #2c3e50
  
  margin-top 60px
</style>
