
<script>
import AppHeader from './components/AppHeader.vue'
import AppContent from './components/AppContent.vue'
import AppFeatures from './components/AppFeatures.vue'
import AppLinks from './components/AppLinks.vue'
import AppFooter from './components/AppFooter.vue'

export default {
  name: 'App',
  components: {
    AppHeader,
    AppContent,
    AppFeatures,
    AppLinks,
    AppFooter
  }
}
</script>





<template>
  <AppHeader></AppHeader>
  <AppContent></AppContent>
  <AppFeatures></AppFeatures>
  <AppLinks></AppLinks>
  <AppFooter></AppFooter>
</template>


<style>
body {
  font-style: sans-serif;
  margin: 0;
}
</style>