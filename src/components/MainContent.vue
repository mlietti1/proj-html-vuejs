<script>
import cards from '../assets/data/courses';
import CourseCard from './CourseCard.vue';
export default {
  name: 'MainContent',
  components:{
    CourseCard
  },
  data(){
    return {
      cards,
      cardCounterMin: 1,
      cardCounterMax: 3
    }
  },
  methods:{
    slideCard(id){
      this.cardCounterMin = 1;
      this.cardCounterMax = 3;
      console.log(id)
      this.cardCounterMin = id * 3 + 1;
      this.cardCounterMax = this.cardCounterMin + 2;
      console.log(this.cardCounterMin, this.cardCounterMax)
    }
  }
}
</script>

<template>

  <div class="main-wrapper">

    <div class="mc-row">

      <div class="text-box">
        <h5>Everything in <span>MaxCoach</span></h5>
        <h2>Learn about our <span>Work Culture</span> at MaxCoach</h2>
        <p>Spend some time to visit our website or head office and discover our current courses, enrollment procedure, and registration deadline. We're opening new classes every beginning of each month.</p>
        <span>Have a question? <a href="#">Get Free Guide <i class="fa-solid fa-right-long"></i></a></span>
      </div>
      <div class="img-box">
        <img class="primary-img" src="../assets/images/stock-full-hd-10-ohki1ayywq3cqutettrncduujpoaorifqu4relt2ts.jpg" alt="image1">
        <img class="secondary-img" src="../assets/images/about-us-01-ohkia3qg98rq9vg3s0mn2hkflr1migdqdw370qnegc.jpg" alt="image2">
        <img class="effect-square" src="../assets/images/maxcoach-shape-07.png" alt="img-shape1">
        <img class="effect-circle" src="../assets/images/maxcoach-shape-02.png" alt="img-shape2">
        <img class="effect-rectangle" src="../assets/images/maxcoach-shape-08.png" alt="img-shape3">
      </div>
    </div>
    <div class="mc-row justify-content-center">
      <div class="number-box">
        <h3 class="number-big">129+</h3>
        <span>enrolled learners</span>
      </div>
      <div class="number-box">
        <h3 class="number-big">80</h3>
        <span>finished sessions</span>
      </div>
      <div class="number-box">
        <h3 class="number-big">4%</h3>
        <span>satisfaction rate</span>
      </div>
    </div>
    <div class="mc-row">
      <div class="video-box">
        <img class="video-preview" src="../assets/images/stock-full-hd-11-670x450.jpg" alt="video-preview">
        <img class="dotted-circle" src="../assets/images/maxcoach-shape-05.png" alt="dotted-cirlce">
        <div class="custom-circle">
        </div>
        <img class="square" src="../assets/images/maxcoach-shape-07.png" alt="square">
        <img class="youtube-icon" src="../assets/images/icon-youtube-play.png" alt="play">
      </div>
      <div class="text-box">
        <h5>How we work</h5>
        <h2>Upgrade Your Skills  <span>Upgrade Your Life</span></h2>
        <p>Opening up more opportunities in fron of you to get the ticket to more enjoyable door in life. Getting equipped with new skills for new sets of insights into your career. MaxCoach accompany learners in every stage of learning.</p>
        <span><a class="dark" href="#">Download free guidebook <i class="fa-solid fa-right-long"></i></a></span>
      </div>

    </div>

    <div class="mc-row text-center">
      <div class="text-box central">
        <h5>Join maxcoach at best</h5>
        <h2>Latest Online  <span>Courses</span></h2>
      </div>

    </div>

    <div class="card-row">
      <CourseCard v-show="card.id <= this.cardCounterMax && card.id >= this.cardCounterMin" :card="card" v-for="card in cards" :key="card.id" />
    </div>
    <div class="card-dots d-flex">
      <div @click="slideCard(index)" v-for="(n, index) in (cards.length / 3)" :key="index" class="dot" :class="{'active': index === (this.cardCounterMin - 1) / 3}"></div>
    </div>
    <div class="bottom-cta">
      <span>Control your personal preference setting to get notified about appropriate courses. <a href="#">View all courses <i class="fa-solid fa-right-long"></i></a></span>
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
  .mc-row {
    .number-box{
      text-align: center;
      margin: 5rem 4rem;
      h3{
        color: $green;
        font-size: 2.5rem;
        font-weight: 600;
      }
      span {
        color: $secondary-font-color;
        font-size: 1rem;
        font-weight: 600;
        text-transform: uppercase;
      }
    }
  }

  .mc-row{
    .video-box{
      width: 57%;
      position: relative;
      .video-preview{
        width: 100%;
      }
      .dotted-circle{
        position: absolute;
        width: 25%;
        right: 90%;
        top: 10%;
        z-index: -1;
      }
      .custom-circle{
        width: 25%;
        aspect-ratio: 1/1;
        border-radius: 50%;
        background-color: rgb(233, 233, 233);
        position: absolute;
        z-index: -2;
        bottom: 75%;
        right: 83%;
      }
      .square {
        position: absolute;
        width: 25%;
        top: 80%;
        left: 80%;
        z-index: -1;
      }
      .youtube-icon{
        width: 15%;
        position: absolute;
        left: 0;
        right: 0;
        top: 0;
        bottom: 0;
        margin: auto;
      }
    }
  }
  .mc-row {
    .text-box.central{
      padding-top: 4rem;
      width: 100%;
      margin: 1rem 0;
    }
  }
  .card-row{
    width: 100%;
    overflow: hidden;
    display: flex;
    justify-content: space-between;
  }
  .card-dots{
    @include centerFlex('horizontal');
    margin: 3rem 0;
    .dot{
      width: 7px;
      height: 7px;
      margin: 0 0.5rem;
      border-radius: 50%;
      background-color: lightgray;
      cursor: pointer;
    }
    .dot.active {
      background-color: $primary-font-color;
      transform: scale(1.5);
    
    }
  }
  .bottom-cta {
    padding: 2rem 0;
    text-align: center;
    margin: 0 auto;
    width: 50%;
    span{
      a{
        color: $primary-font-color;
        font-weight: 600;
        text-decoration-color: lightgray;
        i{
          text-decoration: underline;
          text-decoration-color: lightgray;
        }
      }
    }
  }
}

</style>