<template>
  <TheHeader />
  <TheNav />
  <TheCarousselle />
  <TheLanguage/>
  <TheFooter />
</template>


<script>
import TheHeader from './components/TheHeader.vue';
import TheNav from './components/TheNav.vue';
import TheFooter from './components/TheFooter.vue';
import TheCarousselle from './components/TheCarousselle.vue'
import TheLanguage from './components/TheLanguage.vue';


export default {
name: 'App',
components: {
  TheHeader,
  TheNav,
  TheFooter,
  TheCarousselle,
  TheLanguage,
}
}
</script>

<style>
</style>