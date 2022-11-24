<script>
import links from '../assets/data/headerLinks';
export default {
  name: 'AppHeader',
  data(){
    return{
      links
    }
  }
}
</script>

<template>
  <header>
    <div class="container">
      <nav>
        <ul class="nav">
          <li v-for="(link, index) in links" :key="index" class="nav-item">
            <a class="nav-link" aria-current="page" href="#">{{link.text}}</a>
          </li>
        </ul>
      </nav>
      <div class="logo">
        <img src="" alt="">
      </div>
    </div>
  </header>
</template>

<style lang="scss" scoped>
@use '../assets/styles/partials/vars' as *;



</style>