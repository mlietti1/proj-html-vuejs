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
    <span class="role">{{card.role}}</span>
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
  background-color: transparent;
  .card-body{
    padding: 1rem 0;
    .role{
      text-transform: uppercase;
      color: $secondary-font-color;
    }
    .card-title{
      margin: 1.5rem 0;
    }
    span{
      margin-right: 1rem;
      color: $secondary-font-color;
      i{
        margin-right: 5px;
      }
    }
  }
}

</style>