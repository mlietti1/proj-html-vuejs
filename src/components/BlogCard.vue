<script>
export default {
  name: 'BlogCard',
  props:{
    card: Object
  },
  methods:{
    getImage(imageName) {
      return new URL(`../assets/images/${imageName}`, import.meta.url).href
    }
  }
}
</script>

<template>
  <div class="card">
  <img :src="getImage(card.imgPath)" class="card-img-top" :alt="card.role">
  <div class="card-body">
    <span>{{card.role}}</span>
    <h5 class="card-title">{{card.title}}</h5>
    <span><i class="fa-solid fa-calendar"></i> {{card.date}}</span>
    <span><i class="fa-solid fa-eye"></i> {{card.views}}</span>
  </div>
</div>
</template>

<style lang="scss" scoped>

@use '../assets/styles/partials/mixin' as *;
@use '../assets/styles/partials/vars' as *;

.card{
  width: 30%;
  border: none;
  .card-body{
    .card-text{
      min-height: 3rem;
    }
  }
}

</style>