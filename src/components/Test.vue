<template lang="pug">
  .test
    input(type="text" v-model="title")
    br
    h1=`{{title}}`

    p(v-if="showFirst" v-text="user.firstName")
    p(v-else v-text="user.notWorthy")
    p(v-if="showLast" v-text="user.lastName")
    p(v-else v-text="user.notWorthy")

    ul
      li(v-for="jam in jams" v-text="jam.title")

    button(v-on:click="greet('Vietnam')") Good Morning
    
    input(type="text" v-on:keyup="pressKey" v-on:keyup.enter="enterHit")
    hr
    
    label First Name
    input(type="text" v-model="user.firstName")
    br
    label Last Name
    input(type="text" v-model="user.lastName")

    h3(v-text="fullName")
    h2(v-text="msg")

</template>


<script>
export default {
  name: 'test',
  props: {
    msg: {
      type: String,
      default: 'FooBar'
    }
  },
  data () {
    return {
      title: 'Hello from the Other Side',
      user: {
        firstName: 'Bob',
        lastName: 'Dylan',
        notWorthy: 'Not Worthy'
      },
      showFirst: false,
      showLast: true,
      jams: [
        {title: 'Hurricane'},
        {title: 'Highway 61 Revisited'},
        {title: 'Like a Rolling Stone'}
      ]
    }
  },
  methods: {
    greet: function (greeting) {
      alert(greeting || 'Hey!')
    },
    pressKey: function (evt) {
      console.log(evt.target.value)
    },
    enterHit: function () {
      console.log('You hit enter!')
    }
  },
  computed: {
    fullName: function () {
      return this.user.firstName + ' ' + this.user.lastName
    }
  }
}
</script>


<style lang="stylus" scoped>
ul
  list-style none
</style>