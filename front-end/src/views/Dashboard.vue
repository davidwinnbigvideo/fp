<template>
    <div class="dashboard">
      <tic-tac-toe />
      <div>
        <br>
      <center>Add a photo of your game to your account!</center>
      </div>
        <MyPhotos v-if="user" />
        <Login v-else />
    </div>
</template>

<script>
import MyPhotos from '@/components/MyPhotos.vue';
import Login from '@/components/Login.vue';
import axios from 'axios';
export default {
  name: 'dashboard',
  components: {
    MyPhotos,
    Login,
  },
  async created() {
      let response = await axios.get('/api/users');
      this.$root.$data.user = response.data.user;
  },
  computed: {
    user() {
      return this.$root.$data.user;
    }
  }
}
</script>

<style scoped>
.dashboard {
  padding-top: 10px;
}
</style>