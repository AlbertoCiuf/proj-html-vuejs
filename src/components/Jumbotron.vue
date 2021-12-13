<template>
  <section class="jumbotron">
    <div class="container">
      <!-- jumbo-top -->
      <div class="jumbo-top">
        <div class="intro">
          <div class="label">Development</div>
          <h2>A Complete Developer Toolset</h2>
          <p>Launch your campaign and benefit from our expertise on designing and managing conversion centered bootstrap4 html page.</p>
          <div class="btn btn-dark">Get Started</div>
          <div class="btn btn-light">Documentation</div>
          <small>Current Version: v2.6.0</small>
        </div>
        <div class="jumbo-img">
          <img src="../assets/img/about.png" alt="About">
        </div>
      </div>
      
      <!-- jumbo bottom collegamenti -->
      <div class="jumbo-bottom">
        jbot
    </div>
    </div>
  </section>
</template>

<script>
export default {
  name:'Jumbotron'
}
</script>

<style lang="scss">
@import '../assets/style/vars.scss';

  section.jumbotron {
    background-color: $bg-color;
    .container {
      padding-top: 50px;
      width: 60%;
      margin: 0 auto;
      .jumbo-top {
        display: flex;
        align-items: center;
        height: 500px;
        .intro {
          width: 50%;
          margin-right: 30px;
          h2 {
            font-size: 56px;
            padding: 15px 0;
          }
          .btn-dark {
            margin-left: 0;
          }
          p, small {
            color: #8492A6;
          }
          p {
            font-size: 18px;
            padding-bottom: 20px;
          }
          small {
            display: block;
            padding-top: 10px;
          }
        }
        .jumbo-img {
          width: 50%;
          img {
          width: 90%;
          }
        } 
      }
    }
  }
</style>