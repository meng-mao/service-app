<template>
  <div class="friend-card" v-for="friend in friends" :key="friend">
    <div class="fullName">
        <h3>{{friend.firstName}}-{{friend.lastName}}</h3>
    </div>
    <div class="comment">
        <p>{{friend.comment}}</p>
    </div>
  </div>
</template>

<script>

export default {
    props:["friends"]
}
</script>

<style>

</style>