<template>
  <footer>
    <!-- footer social, links, newsletter -->
    <div class="container">
      <div class="footer-top">
        <div class="social-area">
          <div class="logo">
            <img src="../assets/img/logo-light.png" alt="Logo light">
          </div>
          <p>Start working with Landrick that can provide everything you need to generate awareness, drive traffic, connect.</p>
          <div class="social-links">
            <i class="fab fa-facebook-f"></i>
            <i class="fab fa-instagram"></i>
            <i class="fab fa-twitter"></i>
            <i class="fab fa-linkedin-in"></i>
          </div>
        </div>

        <div class="f-links">
          <div class="company">
            <h3>Company</h3>
            <ul>
              <li>link footer</li>
              <li>link footer</li>
              <li>link footer</li>
              <li>link footer</li>
              <li>link footer</li>
              <li>link footer</li>
              <li>link footer</li>
              <li>link footer</li>
              <li>link footer</li>
              <li>link footer</li>
              <li>link footer</li>
              <li>link footer</li>
              <li>link footer</li>
            </ul>
          </div>

          <div class="useful">
            <h3>Useful links</h3>
            <ul>
              <li>link footer</li>
              <li>link footer</li>
              <li>link footer</li>
              <li>link footer</li>
              <li>link footer</li>
              <li>link footer</li>
              <li>link footer</li>
              <li>link footer</li>
              <li>link footer</li>
              <li>link footer</li>
            </ul>
          </div>
        </div>

        <div class="f-newsletter">
          <h3>Newsletter</h3>
          <p>Sign up and receive the latest tips via email.</p>
          <strong>Write your email <span class="red">*</span></strong> <br>
          <i class="far fa-envelope"></i>
          <input type="text" placeholder="Your email:">
          <div class="btn btn-dark">Subscribe</div>
        </div>

      </div>
    </div>

    <div class="border-bottom"></div>

    <!-- footer bot -->
    <div class="footer-bottom">
      <div class="container">
        aaa
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  name: 'Footer',
}
</script>

<style lang="scss" scoped>
@import '../assets/style/vars.scss';

footer {
  background-color: #1F2942;
  .container {
    width: 60%;
    margin: 0 auto;
    .footer-top {
      display: flex;
      justify-content: space-between;
      gap: 50px;
      padding: 50px 0;
      h3 {
        color: #fff;
        font-weight: 400;
        padding-bottom: 20px;
      }
      p, i, strong {
        color: $light-text-color;
      }
      span.red {
        color: #E43F52;
      }
      .social-area {
        width: calc(100% / 3);
        .logo {
          img {
            width: 120px;
          }
        }
        p, .social-links {
          padding: 15px 0;
        }
        .social-links {
          i {
          border: 1px solid $light-text-color;
          border-radius: 5px;
          padding: 8px 10px;
          margin-right: 5px;
         }
        } 
      }
      .f-links {
        width: calc(100% / 3);
        display: flex;
        gap: 70px;
        ul li {
          color: $light-text-color;
        }
      }
      .f-newsletter {
        width: calc((100% / 3) / 1.5);
        p {
          padding-bottom: 20px;
        }
        i.fa-envelope {
          background-color: #26314F;
          border: 1px solid $light-text-color;
          border-radius: 10px;
          padding: 10px 7px;
          border-right: none;
          vertical-align: middle;
          width: 30px;
          border-top-right-radius: 0;
          border-bottom-right-radius: 0;
          z-index: 2;
        }
        input {
          color: $light-text-color;
          z-index: 1;
          width: calc(100% - 30px);
          vertical-align: middle;
          border-left: none !important;
          border-top-left-radius: 0 !important;
          border-bottom-left-radius: 0 !important;
          background-color: #26314F;
          border: 1px solid $light-text-color;
          margin: 10px 0;
          padding: 10px;
          border-radius: 10px;
          &::placeholder {
            color: $light-text-color;
          }
        }
        .btn.btn-dark {
          width: 100%;
          margin: 0;
          margin-top: 10px;
          text-align: center;
          color: $active-link-color;
          background-color: #222F52;
          transition: all .2s;
          &:hover {
            color: $light-text-color;
          }
        }
      }
    }
  }
  
}

</style>