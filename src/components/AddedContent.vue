<script>
import BlogCard from './BlogCard.vue';
import cards from '../assets/data/blogs'
export default {
  name: 'AddedContent',
  components:{
    BlogCard
  },
  data(){
    return{
      cards
    }
  }
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
        <div class="back top position-absolute">
          <h5>Professional team of specialists and passionate mentors at reach</h5>
          <p>I need to get a certification for English proficiency and MaxCoach is my best choice. Their tutors are smart and professional when dealing with students.</p>
          <img class="icon" src="../assets/images/testimonial-avata-01.jpg" alt="avatar">
          <div class="info">
            <h4>Madley Pondor</h4>
            <span>/ IT Specialist</span>
          </div>
        </div>
        <div class="back bottom position-absolute">
          <h5>Professional team of specialists and passionate mentors at reach</h5>
          <p>I need to get a certification for English proficiency and MaxCoach is my best choice. Their tutors are smart and professional when dealing with students.</p>
          <img class="icon" src="../assets/images/testimonial-avata-02.jpg" alt="avatar">
          <div class="info">
            <h4>Mina Hollace</h4>
            <span>/ Freelancer</span>
          </div>
        </div>
      </div>
    </div>
    <div class="mc-row py-5">
      <div class="img-box position-relative">
        <img class="propic first" src="../assets/images/testimonial-avata-01.jpg" alt="avatar1">
        <img class="propic second" src="../assets/images/testimonial-avata-02.jpg" alt="">
        <img class="propic third" src="../assets/images/testimonial-avata-03.jpg" alt="">
        <img class="shape1" src="../assets/images/maxcoach-shape-05.png" alt="">
        <img class="shape2" src="../assets/images/maxcoach-shape-07.png" alt="">
        <img class="shape3" src="../assets/images/maxcoach-shape-01.png" alt="">
      </div>
      <div class="text-box">
        <h5>Everything in <span>MaxCoach</span></h5>
        <h2>We're Here To <span>Transform</span> You!</h2>
        <p>As learners people can enjoy great companionship from MaxCoach mentors and educators. We can help you develop and grow at your best.</p>
        <a class="button" href="#">Get Free Guide</a>
      </div>
    </div>
  </div>
  <div class="grey-bg">
    <div class="main-wrapper">
      <div class="mc-row text-center">
        <div class="text-box central">
          <h5>read for more joyment</h5>
          <h2>Latest from  <span>Our Blogs</span></h2>
        </div>
      </div>
      <div class="card-row">
        <BlogCard :card="card" v-for="(card, index) in cards" :key="index"/>
      </div>

    </div>
  </div>
  <div class="main-wrapper">
    <div class="mc-row input-wrapper">
      <div class="text-box">
        <h2 class="mb-5">Subscribe <span>Newsletters</span></h2>
        <p>Enter your email address to register to our newsletter subscription delivered on a regular basis!</p>
        <input class="mt-5" type="text" placeholder="Enter your email">
        <button>Subscribe</button>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
@use '../assets/styles/partials/mixin' as *;
@use '../assets/styles/partials/vars' as *;

.main-wrapper, .grey-bg, .input-wrapper{
  width: 60%;
  margin: 50px auto;
  color: $primary-font-color;
  .mc-row{
    @include centerFlex('vertical');
    width: 100%;
    justify-content: space-between;
    margin: 5rem 0;
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
      a.button {
        text-decoration: none;
        color: white;
        background-color: $green;
        padding: 0.8rem 2.5rem;
        border: 2px solid white;
        font-size: 0.8rem;
        font-weight: 600;
        margin-top: 1.3rem;
        display: inline-block;
        border-radius: 5px;
      }
    }
    
  }
  .graphics{
    width: 60%;
    .front, .back{
      background-color: white;
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
  .back{
    z-index: -1;
    opacity: 0.7;
    left: 0;
    right: 0;
    margin: auto;
    transform: scale(0.8);
  }
  .back.top{
    bottom: 30%;
  }
  .back.bottom {
    top: 30%;
  }
  .mc-row{
    .img-box{
      width: 60%;
      min-height: 500px;
      img{
        border-radius: 5px;
      }
      img.propic{
        width: 25%;
        position: absolute;
      }
      .propic.first{
        top: 30%;
        right: 30%;
        z-index: 1;
      }
      .propic.second{
        top: 60%;
        right: 50%;
        z-index: 2;
      }
      .propic.third{
        top: 40%;
        right: 70%;
        z-index: 3;
      }
      .shape1{
        position: absolute;
        width: 25%;
        z-index: 0;
        top: 5%;
        right: 20%;
      }
      .shape2{
        position: absolute;
        width: 25%;
        z-index: 0;
        top: 50%;
        right: 40%;
      }
      .shape3{
        position: absolute;
        width: 20%;
        top: 80%;
        right: 100%;
      }
    }
  }
}

.grey-bg{
  margin: 0;
  padding: 50px 0;
  width: 100%;
  background-color: $light-bg;
  .mc-row{
    .text-box.central{
      width: 100%;
      margin: 1rem 0;
    }
  }
  .card-row{
    width: 100%;
    display: flex;
    justify-content: space-between;
  }
  
}

.main-wrapper{
  .input-wrapper{
    text-align: center;
    width: 50%;
    margin: 0 auto;
    .text-box{
      width: 100%;
      input{
        padding-left: 1.2rem;
        margin-left: 0.7rem;
        height: 3rem;
        border: none;
        background-color: #f8f8f8;
        border-bottom-left-radius: 5px;
        border-top-left-radius: 5px;
        width: 450px;
      }
      button{
        background-color: $green;
        height: 3rem;
        border: none;
        border-top-right-radius: 5px;
        border-bottom-right-radius: 5px;
        padding: 0 1rem;
        color: white;
        &:active{
          
          background-color: lighten($green, $amount: 10%);
        }
      }
    }
  }
}

</style>