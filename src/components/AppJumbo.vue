<script>
  export default {
    name: 'AppJumbo'
  }
</script>

<template>
  <div class="jumbotron d-flex ">
    <div>
      <h3>Commence Business</h3>
      <h1>Distant Mentoring Program</h1>
      <a class="button" href="#">Download free guidebook<i class="fa-solid fa-right-long"></i></a>
    </div>
    <div class="fixed-menu">
      <nav>
        <ul class="d-flex">
          <li>
            <a href="#"><i class="fa-solid fa-ruler-combined"></i></a>
          </li>
          <li>
            <a href="#"><i class="fa-solid fa-life-ring"></i></a>
          </li>
          <li>
            <a href="#"><i class="fa-solid fa-book"></i></a>
          </li>
          <li>
            <a href="#"><i class="fa-solid fa-cart-shopping"></i></a>
          </li>
        </ul>
      </nav>
    </div>
  </div>
</template>

<style lang="scss" scoped>
@use '../assets/styles/partials/vars' as *;
@use '../assets/styles/partials/mixin'as *;
.jumbotron{
  @include centerFlex('both');
  text-align: center;
  height: 670px;
  background-image: url('../assets/images/home-3-hero-bg.jpg');
  background-size: cover;
  color: white;
  h3{
    font-size: 1.7rem;
    font-weight: 600;
  }
  h1{
    font-size: 3.8rem;
    font-weight: 300;
  }
  a.button {
    text-decoration: none;
    color: $green;
    background-color: white;
    padding: 0.8rem 2.5rem;
    border: 2px solid white;
    font-size: 0.8rem;
    font-weight: 600;
    margin-top: 1.3rem;
    display: inline-block;
    border-radius: 5px;
    cursor: pointer;
    &:hover {
      color: white;
      background-color: $green;
      border-color: $green;
    }
    &:active {
      border-left: 2px solid darken($green, $amount: 20%);
      border-top: 2px solid darken($green, $amount: 20%);
      border-bottom: 2px solid lighten($green, $amount: 20%);
      border-right: 2px solid lighten($green, $amount: 20%);
    }
    i{
      margin-left: 10px;
    }
  }
  .fixed-menu {
    position: fixed;
    top: 30vh;
    right: 0;
    nav {
      ul{
        @include flexCol;
        list-style: none;
        li{
          a{
            background-color: white;
            color: $primary-font-color;
            display: inline-block;
            line-height: 2.2rem;
            width: 2.2rem;
            height: 2.2rem;
            text-align: center;
            &:hover {
              color: white;
              background-color: black;
            }
            &:active{
              filter: invert(1);
            }   
          }
          &:first-child a {
            border-top-left-radius: 5px;
          }
          &:last-child a{
            border-bottom-left-radius: 5px;
          }         
        }
      }
    }
  }
}

</style>