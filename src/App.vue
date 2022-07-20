<template>
  <Nav />
  <Form></Form>
</template>

<script>

import Nav from "./components/FriendNav.vue"
import Form from "./components/FriendForm.vue"
export default {
  
  components: {
    Nav,
    Form,
  }
}
</script>

<style>
#app{
  font-family: sans-serif;
  width: 50%;
  margin: auto;
  padding: 10px;
}
</style>
