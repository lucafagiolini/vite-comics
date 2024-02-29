
<script>
import AppHeader from './components/AppHeader.vue'
import AppContent from './components/AppContent.vue'

export default {
  name: 'App',
  components: {
    AppHeader,
    AppContent
  }
}
</script>





<template>
  <AppHeader></AppHeader>
  <AppContent></AppContent>
</template>


<style>
body {
  font-style: sans-serif;
  margin: 0;
}
</style>