<script>

import AppJumbo from './AppJumbo.vue';
import MainContent from './MainContent.vue';
import AddedContent from './AddedContent.vue';
import AppFooter from './AppFooter.vue';
export default {
  name: 'AppMain',
  components:{
    AppJumbo,
    MainContent,
    AddedContent,
    AppFooter
  }
}
</script>

<template>

  <main>
    <AppJumbo />
    <div class="content-bg">
      <MainContent />
    </div>
    <div class="content-bg-white">
      <AddedContent />
    </div>
    <AppFooter />

  </main>
</template>

<style lang="scss" scoped>
@use '../assets/styles/partials/mixin' as *;
@use '../assets/styles/partials/vars' as *;
.content-bg{
  padding: 190px 0;
  background-image: linear-gradient(white, $light-bg);
}
.content-bg-white{
  padding: 100px 0;
}



</style>