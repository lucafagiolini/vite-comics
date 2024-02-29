
<script>
import AppHeader from './components/AppHeader.vue'
import AppContent from './components/AppContent.vue'
import AppFeatures from './components/AppFeatures.vue'

export default {
  name: 'App',
  components: {
    AppHeader,
    AppContent,
    AppFeatures
  }
}
</script>





<template>
  <AppHeader></AppHeader>
  <AppContent></AppContent>
  <AppFeatures></AppFeatures>
</template>


<style>
body {
  font-style: sans-serif;
  margin: 0;
}
</style>