<template>
  <TheHeader />
  <TheNav />
  <TheLanguage />
  <TheContact />
  <TheFooter />
</template>

<script>
import TheHeader from './components/TheHeader.vue';
import TheNav from './components/TheNav.vue';
import TheFooter from './components/TheFooter.vue';
import TheLanguage from './components/TheLanguage.vue';
import TheContact from './components/TheContact.vue';

export default {
  name: 'App',
  components: {
    TheHeader,
    TheNav,
    TheFooter,
    TheLanguage,
    TheContact
  }
}
</script>