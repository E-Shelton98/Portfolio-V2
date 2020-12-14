<template>
  <div class="bg-gradient-to-b from-green-200 via-indigo-400 to-purple-400 p-2">
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
