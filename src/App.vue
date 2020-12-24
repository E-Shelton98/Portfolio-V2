<template>
  <div class="bg-gray-800 p-2 flex flex-col items-center">
    <AppHome/>
    <ContactMe/>
  </div>
</template>

<script>

import AppHome from './components/AppHome.vue'
import ContactMe from './components/ContactMe.vue'

export default {
  name: 'App',
  components: {
    AppHome,
    ContactMe
  }
}
</script>

<style>

</style>
