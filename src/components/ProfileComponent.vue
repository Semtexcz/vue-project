<template>
  <div>
      <p>Profil komponenta</p>
      <button @click="moveToUsers()">Users</button>
  </div>
</template>

<script>
export default {
    methods: {
        moveToUsers(){
            this.$router.push("/users")
        }
    }
}
</script>

<style>

</style>