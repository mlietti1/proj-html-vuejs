<script>
export default {
  name: 'MainContent'
}
</script>

<template>

  <div class="main-wrapper">

    <div class="mc-row">

      <div class="text-card">
        <h5>Everything in <span>MaxCoach</span></h5>
        <h2>Learn about our <span>Work Culture</span> at MaxCoach</h2>
        <p>Spend some time to visit our website or head office and discover our current courses, enrollment procedure, and registration deadline. We're opening new classes every beginning of each month.</p>
        <span>Have a question? <a href="#">Get Free Guide </a></span>
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

  .mc-row{
    .text-card{
      width: 40%;
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
        font-size: 3rem;
        margin: 1rem 0;
      }
    }

  }
}

</style>