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
              <li v-for="(link, index) in companyLinks" :key="`companyLink${index}`">
                <a :href="link.href">{{link.name}}</a>
              </li>
            </ul>
          </div>

          <div class="useful">
            <h3>Useful links</h3>
            <ul>
              <li v-for="(link, index) in usefulLinks" :key="`useful${index}`">
                <a :href="link.href">{{link.name}}</a>
              </li>
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
    <div class="container">
      <div class="footer-bottom">
        <div class="copyright">
          <p>&copy; 2020 Landrick. Design with <span class="red"><i class="fas fa-heart"></i></span> by Shreethemes.</p>
        </div>
        <div class="payments">
          <img src="../assets/img/american-ex.png" alt="american express">
          <img src="../assets/img/discover.png" alt="discover">
          <img src="../assets/img/master-card.png" alt="master card">
          <img src="../assets/img/paypal.png" alt="paypal">
          <img src="../assets/img/visa.png" alt="visa">
        </div>
      </div>
    </div>
    <div class="go-top" @click="goTop">
      <i class="fas fa-arrow-up"></i>
    </div>
  </footer>
</template>

<script>
export default {
  name: 'Footer',
  props: {
    companyLinks: Array,
    usefulLinks: Array
  },
  methods: {
    goTop(){
      window.scroll({
        top: 0,
        left: 0,
        behavior: 'smooth'
      });
    }
  }
}
</script>

<style lang="scss" scoped>
@import '../assets/style/vars.scss';

footer {
  background-color: #1F2942;
  position: relative;
  .container {
    width: 60%;
    margin: 0 auto;
    span.red {
      color: #E43F52;
    }
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
          cursor: pointer;
          transition: all .2s;
          &:hover{
            color: #fff;
            background-color: $light-text-color;
           }
         }
        } 
      }
      .f-links {
        width: calc(100% / 3);
        display: flex;
        gap: 70px;
        ul li {
          color: $light-text-color;
          padding: 5px 0;
          &::before {
            content: '\f054';
            font-weight: 900;
            font-family: 'Font Awesome 5 Free';
            padding-right: 5px;
            font-size: 10px;
          }
          &:hover{
            color: #fff;
          }
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

    .footer-bottom {
      height: 80px;
      display: flex;
      justify-content: space-between;
      align-items: center;
      .copyright p {
        color: $light-text-color;
        .red i {
          font-size: 14px;
        }
      }
      .payments img {
        width: 30px;
        vertical-align: middle;
        border: 1px solid black;
        margin: 1px;
      }
    }
  }
  .go-top i {
    position: absolute;
    right: 40px;
    bottom: 20px;
    background-color: $active-link-color;
    border-radius: 5px;
    color: #fff;
    padding: 10px;
    font-size: 14px;
    cursor: pointer;
    transition: all .2s;
    &:hover{
      transform: scale(1.2);
    }
  }
  .border-bottom {
    background-color: darken($light-text-color,30);
  }

}

</style>