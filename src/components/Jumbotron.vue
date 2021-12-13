<template>
<div class="wrapper">

  <section class="jumbotron">
    <div class="container">
      <!-- jumbo-top -->
      <div class="jumbo-top">
        <div class="settings">
          <i class="fas fa-cog"></i>
        </div>
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
    </div>
      <div class="border-bottom"></div>
      <!-- jumbo bottom collegamenti -->
      <div class="container bot">
        <div class="jumbo-bottom">
          <ul>
            <li><img src="../assets/img/amazon.svg" alt=""></li>
            <li><img src="../assets/img/google.svg" alt=""></li>
            <li><img src="../assets/img/lenovo.svg" alt=""></li>
            <li><img src="../assets/img/paypal.svg" alt=""></li>
            <li><img src="../assets/img/shopify.svg" alt=""></li>
            <li><img src="../assets/img/spotify.svg" alt=""></li>

          </ul>
        </div>
      </div>
  </section>
  <div class="rounded-borders"></div>
</div>
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

      &.bot {
        padding: 0;
      }
      .jumbo-top {
        position: relative;
        display: flex;
        align-items: center;
        height: 500px;
        margin-bottom: 100px;
        .settings {
          cursor: pointer;
          position: absolute;
          top: 0;
          left: -385px;
          width: 40px;
          height: 35px;
          background-color: #fff;
          border-radius: 0 50% 50% 0;
          border: 1px solid lighten(#8492A6, 30);
          transition: all .3s;
          i.fa-cog {
            color: $active-link-color;
            font-size: 20px;
            padding-left: 10px;
            line-height: 35px;
          }
          &:hover{
            transform: scale(1.2);
          }
        }
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
      
      .jumbo-bottom {
        height: 70px;
        ul {
          display: flex;
          height: 100%;
          padding-top: 35px;
          li {
            width: calc(100%/6 - 10px);
            img {
              height: 30px;
            }
          }
        }
      }
    }
  }
    
</style>