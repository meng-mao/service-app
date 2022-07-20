<template>
  <form>
    <div class="form-group">
      <input v-model="firstName" type="text" placeholder="First Name" />
    </div>
    <div class="form-group">
      <input v-model="lastName" type="text" placeholder="Last Name" />
    </div>
    <div class="form-group">
      <input v-model="comment" type="text" placeholder="Comment" />
    </div>
    <div class="form-group">
      <button @click="AddFriend">ADD</button>
    </div>
    <FriendCard :friends="friends"></FriendCard>
  </form>
</template>

<script>
import FriendCard from "./FriendCard.vue";
export default {
    components: {
       FriendCard,
       },
    data() {
        return {
            firstName: "",
            lastName: "",
            comment: "",
            friends: [],
        };
    },
    methods: {
        AddFriend(event) {
            event.preventDefault();
            let friendList = {};
            friendList.firstName = this.firstName.toUpperCase();
            friendList.lastName = this.lastName.toUpperCase();
            friendList.comment = this.comment;
            if (this.firstName !== "" && this.lastName !== "" && this.comment !== "") {
                this.friends.push(friendList);
                console.log(this.friends)
            }
        }
    },
    
}
</script>

<style>
form {
  box-shadow: rgba(99, 99, 99, 0.2) 0px 2px 8px 0px;
  padding: 15px;
  width: 70%;
  margin: auto;
}

input {
  width: 96%;
  margin-bottom: 5%;
  padding: 1.5%;
}

button {
  width: 100%;
  padding: 1.5%;
  background: rgb(142, 142, 142);
  border: none;
  color: #fff;
}
</style>