<template lang="pug">
  .test
    h1=`{{title}}`
    p(v-if="showFirst" v-text="user.firstName")
    p(v-if="showLast" v-text="user.lastName")
</template>


<script>
export default {
  name: 'test',
  data () {
    return {
      title: 'Hello from the Other Side',
      user: {
        firstName: 'Bob',
        lastName: 'Dylan'
      },
      showFirst: true,
      showLast: true
    }
  }
}
</script>


<style lang="stylus" scoped>

</style>