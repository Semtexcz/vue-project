<template>
  <div>
      <img src="https://hips.hearstapps.com/countryliving.cdnds.net/17/47/1511194376-cavachon-puppy-christmas.jpg">
      <img src="https://d1aeh7hxqn8xf9.cloudfront.net/wp-content/uploads/2019/12/FRFTS-Dec-MarysLittleLamb.jpg">
      <br>
      <input v-model="inputText">
      <p>{{ inputText }}</p>
      <pre>{{store}}</pre>
      <pre>{{store.doubleCount}}</pre>
      <button @click="editStore()">Edit store</button>
      <button @click="resetStore()">Reset store</button>
  </div>
</template>

<script>
import {useStore} from '@/stores/store' //@ znamená src

export default {
  setup(){ //Composition API
    const store = useStore()

    return {
      store
    }
  },
  data(){
    return {
      inputText: ""
    }
  },
  methods:{
    editStore() {
      this.store.counter = 69
      console.log(this.store.counter)
    },
    resetStore() {
      this.store.$reset()
      console.log(this.store.counter)
    }
  }
}
</script>

<style>
img {
  max-width: 400px;
}
</style>