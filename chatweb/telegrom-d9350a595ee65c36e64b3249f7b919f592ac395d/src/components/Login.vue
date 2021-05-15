<template>
  <div class="chat-list">
    <h3>Usuarios</h3>
    <user-list-item
      v-for="user in $store.state.user.list"
      :key="user._id"
      :id="user._id"
      :name="user.name"
    />
  </div>
</template>

<script>
import axios from 'axios';
import UserListItem from '@/components/UserListItem.vue';

export default {
  name: 'ChatList',
  components: {
    UserListItem,
  },
  created() {
    // this.$store.dispatch('user/getUsers');
    console.log('Hola mundo desde axios');
    this.getUsers();
  },
  mounted() {


  },
  methods: {
    async getUsers() {
      console.log('Aqui va la peticion de usuarios');
      await axios.get('http://localhost:4000/users').then((response) => {
        console.log(response);
      }).catch(e => console.log(`errrror:   ${e}`));
    },
  },
};
</script>

<style scoped>
h3 {
  text-align: left;
  padding-left: 16px;
}
</style>
