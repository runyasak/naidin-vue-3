<template>
  <div class="home">
    <img
      alt="Vue logo"
      src="../assets/logo.png"
    >
    <HelloWorld msg="Welcome to Your Vue.js App" />
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue'
import HelloWorld from '@/components/HelloWorld.vue'
import useFetchDbJson from '@/composables/useFetchDbJson'
import bookJson from '../book.json'

export default defineComponent({
  name: 'HomePage',
  components: {
    HelloWorld
  },
  setup() {
    const books = useFetchDbJson(bookJson)

    return {
      books
    }
  }
})
</script>
