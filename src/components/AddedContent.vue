<script>
export default {
  name: 'AddedContent'
}
</script>

<template>
  <div class="main-wrapper">
    <div class="mc-row">
      <div class="text-box">
        <h5>testimonials</h5>
        <h2>Why do peopls <span>*Hearts*</span> Us?</h2>
        <p>Seeking for verbals of our</p>
        <span>Have a question? <a href="#">Get Free Guide <i class="fa-solid fa-right-long"></i></a></span>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
@use '../assets/styles/partials/mixin' as *;
@use '../assets/styles/partials/vars' as *;

.main-wrapper{
  padding-top: 190px;
  width: 60%;
  margin: 0 auto;
  color: $primary-font-color;
  .mc-row{
    @include centerFlex('vertical');
    width: 100%;
    justify-content: space-between;
    margin-bottom: 3rem;
    .text-box{
      width: 35%;
      h5{
        font-weight: 300;
        font-size: 1rem;
        text-transform: uppercase;
        color: $secondary-font-color;
        span{
          font-weight: 600;
        }
      }
      h2{
        font-size: 2.5rem;
        margin: 1rem 0;
        span {
          color: $green;
          font-weight: 300;
        }
      }
      span {
        a {
          color: $green;
          font-weight: 600;
          text-decoration-color: lightgray;
          i{
            text-decoration: underline;
            text-decoration-color: lightgray;
          }
        }
        a.dark{
          color: $primary-font-color;
        }
      }
      
    }
    .img-box{
      position: relative;
      width: 50%;
      .primary-img {
        width: 100%;
        border-radius: 5px;
      }
      .secondary-img{
        position: absolute;
        width: 30%;
        border-radius: 5px;
        bottom: 77%;
        left: 80%;
        z-index: 3;
      }
      .effect-square{
        width: 30%;
        position: absolute;
        z-index: -1;
        bottom: 73%;
        left: 69%;
      }
      .effect-circle{
        position: absolute;
        width: 20%;
        top: 90%;
        left: 70%;
        z-index: 3;
      }
      .effect-rectangle{
        position: absolute;
        width: 30%;
        right: 80%;
        top: 70%;
        z-index: -1;
      }
    } 
  }
}

</style>