<template>
  <div class="avatar-generator">
    <input type="text" placeholder="Ketikkan nama anda.." class="input"><br>
    <button @click="generateAvatar">Buat profile picture</button><br>
    <img :src="avatarUrl" alt="Avatar" />
  </div>
</template>

<script>
export default {
  data() {
    return {
      avatarUrl: ""
    };
  },
  methods: {
    generateAvatar() {
      const hash = Math.random().toString(36).substring(7);
      this.avatarUrl = `https://robohash.org/${hash}`;
    }
  }
};
</script>

<style scoped>
.avatar-generator {
  text-align: center;
  margin-top: 50px;
}
button, input, img {
  
  padding: 10px 20px;
  font-size: 16px;
}
</style>