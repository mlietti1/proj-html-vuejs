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
    <div class="card-body p-4">
      <h5 class="card-title">{{card.price}}<span>{{card.cents}}</span></h5>
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
    h5{
      font-weight: 600;
      color: $green;
      span{
        font-size: 1rem;
        color: $green;
      }
    }
    .card-text{
      min-height: 5rem;
      font-weight: 600;
    }
    span{
      font-size: 0.8rem;
      margin-right: 1rem;
      color: $secondary-font-color;
      i{
        margin-right: 5px;
      }
    }
  }
}

</style>