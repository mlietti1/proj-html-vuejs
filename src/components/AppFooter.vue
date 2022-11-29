<script>
import socialLinks from '../assets/data/socialLinks';
export default {
  name: 'AppFooter',
  data(){
    return{
      socialLinks
    }
  }
}
</script>

<template>
  <footer>
    <div class="main-wrapper d-flex">
      <div class="footer-left">
        <h5>Address</h5>
        <p>382 NE 191st ST # 87394 Miami, FL 33179-3899</p>
        <p>+1(305) 547-9909 (9am - 5pm EST, Monday - Friday)</p>
        <p>support@maxcoach.com</p>
        <ul class="mc-menu d-flex">
          <li class="me-4" v-for="(link, index) in socialLinks" :key="index">
            <a :href="link.href"><i class="fa-brands" :class="`${link.class}`"></i></a>
          </li>
          
        </ul>
      </div>
      <div class="footer-right d-flex">
        <div class="mc-col">
          <h5>Explore</h5>
          <ul>
            <li><a href="#">Start here</a></li>
            <li><a href="#">Blog</a></li>
            <li><a href="#">About us</a></li>
            <li><a href="#">Success story</a></li>
            <li><a href="">Courses</a></li>
            <li><a href="#">Contact us</a></li>
          </ul>
        </div>
        <div class="mc-col">
          <h5>Information</h5>
          <ul>
            <li><a href="#">Membership</a></li>
            <li><a href="#">Purchase guide</a></li>
            <li><a href="#">Privacy policy</a></li>
            <li><a href="#">Terms of service</a></li>
          </ul>
        </div>
      </div>
    </div>
    <div class="credits">
      <p>&copy; 2020 Maxcoach. All Rights Reserved</p>
    </div>
    <a class="top-scroll" href="#"><i class="fa-solid fa-up-long"></i></a>
  </footer>
</template>

<style lang="scss" scoped>
@use '../assets/styles/partials/mixin' as *;
@use '../assets/styles/partials/vars' as *;

footer{
  position: relative;
  background-color: $dark-bg;
  padding: 5rem 0;
  color: rgba(255, 255, 255, 0.6);
  font-size: 0.8rem;
  height: 400px;
  .main-wrapper{
    width: 60%;
    margin: 0 auto;
    .footer-left, .footer-right{
      width: 50%;
      margin-bottom: 2rem;
      .mc-col{
        margin-right: 80px;
      }
      h5{
        font-size: 1rem;
        color: white;
        font-weight: 600;
      }
      ul{
        list-style: none;
        padding: 0;
        li{
          line-height: 2rem;
          a{
            color: rgba(255, 255, 255, 0.6);
            text-decoration: none;
            &:hover{
              color: white;
            }
            i{
              font-size: 1.5rem;
            }
          }
        }
      }
    }
  }
  .credits{
    width: 100%;
    text-align: center;
  }
  .top-scroll{
    display: inline-block;
    position: absolute;
    right: 2rem;
    bottom: 2rem;
    width: 40px;
    height: 40px;
    line-height: 40px;
    background-color: $green;
    border-radius: 50%;
    text-align: center;
    
    color: white;
    text-decoration: none;
    &:active{
      color: $green;
      background-color: white;
    }
    
  }
}
</style>