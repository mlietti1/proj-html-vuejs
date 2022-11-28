<script>
export default {
  name: 'CourseCard',
  props: {
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
    <img :src="getImage(card.img)" class="card-img-top" :alt="'Course image'">
    <div class="card-body">
      <h5 class="card-title">{{card.price}}{{card.cents}}</h5>
      <p class="card-text">{{card.title}}</p>
      <span><i class="fa-regular fa-file-lines"></i> {{card.lessons}} Lessons</span>
      <span><i class="fa-regular fa-user"></i> {{card.students}} Students</span>
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