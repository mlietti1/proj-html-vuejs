<script>

import AppHeader from './components/AppHeader.vue';
import AppJumbo from './components/AppJumbo.vue';
export default {
  name: 'App',
  components: {
    AppHeader,
    AppJumbo
  }
}
</script>

<template>
  <AppHeader />
  <AppJumbo />
</template>

<style lang="scss">
@use './assets/styles/general'
</style>