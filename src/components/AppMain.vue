<script>

import AppJumbo from './AppJumbo.vue';
import MainContent from './MainContent.vue';

export default {
  name: 'AppMain',
  components:{
    AppJumbo,
    MainContent
  }
}
</script>

<template>
  <AppJumbo />
  <MainContent />
</template>

<style lang="scss" scoped>
@use '../assets/styles/partials/mixin' as *;
@use '../assets/styles/partials/vars' as *;



</style>