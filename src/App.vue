<template>
  <div class="p-2">
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
