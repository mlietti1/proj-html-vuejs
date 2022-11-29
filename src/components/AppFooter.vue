<script>
export default {
  name: 'AppFooter'
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
        <ul>
          <li></li>
        </ul>
      </div>
      <div class="footer-right d-flex">
        <div class="me-5">
          <h5>Explore</h5>
          <ul>
            <li></li>
            <li></li>
            <li></li>
            <li></li>
            <li></li>
            <li></li>
          </ul>
        </div>
        <div>
          <h5>Explore</h5>
          <ul>
            <li></li>
            <li></li>
            <li></li>
            <li></li>
          </ul>
        </div>
      </div>
    </div>
    <div class="credits">
      <p>&copy; 2020 Maxcoach. All Rights Reserved</p>
    </div>
  </footer>
</template>

<style lang="scss" scoped>
@use '../assets/styles/partials/mixin' as *;
@use '../assets/styles/partials/vars' as *;

footer{
  background-color: $dark-bg;
  padding: 5rem 0;
  color: rgba(255, 255, 255, 0.599);
  .main-wrapper{
    width: 60%;
    margin: 0 auto;
    .footer-left, .footer-right{
      width: 50%;
      h5{
        font-size: 1rem;
        color: white;
        font-weight: 600;
      }
    }
  }
  .credits{
    width: 100%;
    text-align: center;
  }
}
</style>