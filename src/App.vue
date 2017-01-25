<template lang="pug">
  #app
    test(msg="How does it feel?")
</template>


<script>
// import Hello from './components/Hello'
import Test from './components/Test'

export default {
  name: 'app',
  components: {
    Test
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
