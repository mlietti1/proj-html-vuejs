<script>

import AppJumbo from './AppJumbo.vue';
import MainContent from './MainContent.vue';
import AddedContent from './AddedContent.vue';
export default {
  name: 'AppMain',
  components:{
    AppJumbo,
    MainContent,
    AddedContent
  }
}
</script>

<template>
  <AppJumbo />
  <div class="content-bg">
    <MainContent />
  </div>
  <div class="content-bg-white">
    <AddedContent />
  </div>
</template>

<style lang="scss" scoped>
@use '../assets/styles/partials/mixin' as *;
@use '../assets/styles/partials/vars' as *;
.content-bg{
  background-image: linear-gradient(white, $light-bg);
}



</style>