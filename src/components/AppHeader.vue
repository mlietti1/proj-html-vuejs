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
    <div class="mc-container row align-items-center d-flex">
      <nav class="col-5">
        <ul class="nav">
          <li @mouseleave="link.active = false" @click="link.active = true" v-for="(link, index) in links" :key="index" class="nav-item position-relative">
            <a class="nav-link" :class="{'active-link': link.active}" aria-current="page" href="#">{{link.text}}</a>
            <div v-show="link.active" class="toggle-menu position-absolute">
              <ul class="p-0">
                <li>Action</li>
                <li>Action</li>
                <li>Action</li>
                <li>Action</li>
              </ul>
            </div>
          </li>
        </ul>
      </nav>
      <div class="logo col-2">
        <img src="../assets/images/dark-logo.png" alt="MaxCoach">
      </div>
      <div class="col-5 search-wrapper text-end">
        <i class="fa-solid fa-cart-shopping"></i>
        <i class="fa-regular fa-circle-user"></i>
        <input placeholder="Search..." type="text">
        <button><i class="fa-solid fa-magnifying-glass"></i></button>
      </div>
    </div>
  </header>
</template>

<style lang="scss" scoped>
@use '../assets/styles/partials/vars' as *;

header {
  height: 80px;
  .mc-container {
    height: 100%;
    nav{
      
      ul{
        li{
          a{
            color: $primary-font-color;
            white-space: nowrap;
            padding: 10px;
            &::after{
              font-family: "Font Awesome 5 Free";
              content: '\f078';
              display: inline-block;
              font-weight: 900;
              font-style: normal;
              font-variant: normal;
              text-rendering: auto;
              -webkit-font-smoothing: antialiased;
              margin-left: 5px;
              font-size: 0.5rem;
              vertical-align: middle;
              line-height: 1rem;
            }
            &:hover{
              color: $green;
            }
          }
          a.active-link {
            color: $green;
          }
          .toggle-menu {
            right: 0;
            & ul{
              list-style: none;
              background-color: white;
              border: 2px solid lightgray;
              border-radius: 5px;
              & li{
                color: $primary-font-color;
                padding: 6px 12px;
                cursor: pointer;
                &:hover{
                  background-color: lightgray;
                }
              }
            }
          }
        }
      }
    }
  }
  .logo{
    text-align: center;
    img {
      height: 26px;
    }
  }
  .search-wrapper {
    i{
      margin: 0.7rem;
    }
    input{
      padding-left: 1.2rem;
      margin-left: 0.7rem;
      height: 3rem;
      border: none;
      background-color: $light-bg;
      border-bottom-left-radius: 5px;
      border-top-left-radius: 5px;
    }
    button{
      background-color: $light-bg;
      height: 3rem;
      border: none;
      border-top-right-radius: 5px;
      border-bottom-right-radius: 5px;
      padding-right: 0.5rem;
      color: $green;
    }
  }
}

</style>