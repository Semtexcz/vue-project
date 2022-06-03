<template>
  <div>
      Ahoj {{ userId }}
      <img v-if="userId == 1" src="https://www.tvguru.cz/wp-content/uploads/2020/08/23/walter/the-batman.jpg">
      <img v-if="userId == 2" src="https://c3.primacdn.cz/sites/default/files/2/66/6038393-sus.jpg">
      <router-view/>
  </div>
</template>

<script>
export default {
   computed: {
    userId() {
      return this.$route.params.id
    }
  },
  created(){
      console.log("Stahuji data...")
  }
}
</script>

<style>

</style>