<template>
  <div>
      <ol>
          <li v-for="user in usersList" :key="user">{{ user }}</li>
      </ol>
  </div>
</template>

<script>
export default {
    name: 'UsersView',
    data(){
        return {
            usersList: ["Brouk Pytlík", "Krteček", "Křemílek", "Vochomůrka", "Křemílek"]
        }
    }
}
</script>

<style scoped>
ol {
    color:deeppink;
    background-color: lightblue
}
</style>
