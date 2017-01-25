<template lang="pug">
  .users
    h1 Users    
    ul
      li(v-for="user in users")=`{{user.name + ":" + user.email}}`
    form(v-on:submit="addUser")
      input(type="text" v-model="newUser.name" placeholder="Enter Name ")
      br
      input(type="text" v-model="newUser.email" placeholder="Enter Email ")
      br
      input(type="submit" value="Submit")

</template>


<script>
export default {
  name: 'users',
  data () {
    return {
      newUser: {},
      users: [
        {
          name: 'Bob Dylan',
          email: 'bob@gmail.com',
          contacted: 'false'
        },
        {
          name: 'Jack White',
          email: 'jack@gmail.com',
          contacted: 'false'
        },
        {
          name: 'CL',
          email: 'CL@gmail.com',
          contacted: 'false'
        }
      ]
    }
  },
  methods: {
    addUser: function (evt) {
      this.users.push({
        name: this.newUser.name,
        email: this.newUser.email,
        contacted: false
      })
      console.log('Add User:' + this.newUser.name)
      evt.preventDefault()
    }
  }
}
</script>


<style lang="stylus" scoped>
.users
  padding-left 50px
  text-align left
ul
  list-style none
</style>