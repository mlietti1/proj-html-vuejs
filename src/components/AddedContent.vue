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
        <p>Seeking for verbals of our service quality? Find them here. Everythimg is transparent and straightforward for your sense of justification.</p>
        <span><a class="dark" href="#">View All <i class="fa-solid fa-right-long"></i></a></span>
      </div>
      <div class="graphics position-relative">
        <div class="front">
          <h5>Professional team of specialists and passionate mentors at reach</h5>
          <p>I need to get a certification for English proficiency and MaxCoach is my best choice. Their tutors are smart and professional when dealing with students.</p>
          <img class="icon" src="../assets/images/testimonial-avata-01.jpg" alt="avatar">
          <div class="info">
            <h4>Madley Pondor</h4>
            <span>/ IT Specialist</span>
          </div>
        </div>
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
    
  }
  .graphics{
    width: 60%;
    .front{
      border-radius: 5px;
      box-shadow: 0 0 40px 10px darken($light-bg, $amount: 10%);
      padding: 3rem;
      h5{
        font-size: 1.2rem;
        font-weight: 600;
        margin-bottom: 2rem;
      }
      p{
        font-size: 1.2rem;
      }
      img {
        width: 12%;
        aspect-ratio: 1/1;
        border-radius: 50%;

      }
      .info {
        display: inline-block;
        margin-left: 2rem;
      
        vertical-align: middle;
        h4{
          text-transform: uppercase;
          font-size: 1.2rem;
        }
        span{
          color: $secondary-font-color;
        }
      }
    }
  }
}

</style>