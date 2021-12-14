<template>
  <main>
    <div class="container">
      <!-- sect key features -->
      <section class="key-features">
        <div class="kf-text">
          <h2>Key Features</h2>
          <p>Start working with <span class="blue">Landrick</span> that can provide everything you need to generate awareness, drive traffic, connect.</p>
        </div>
        <div class="kf-cards">
          <KeyfeaturesCard 
          v-for="(card, index) in kfCardInfo" :key="`kfCard${index}`"
          :cardInfo="card" />
        </div>
      </section>

      <!-- sect quickstart -->
      <section class="quickstart">
        <div class="qs-text">
          <p class="blue">
            Quickstart
          </p>
          <h2>
            Awesome isn't it? Let's dive in!
          </h2>
          <p>Start working with <span class="blue">Landrick</span> that can provide everything you need to generate awareness, drive traffic, connect.</p>
        </div>
        <div class="graph-wrapper">
          <div class="qs-graph">
            <ul>
              <li>npm</li>
              <li>nuget</li>
              <li>spm</li>
              <li>github</li>
            </ul>
            <div class="graph-cmd">
              <p><span class="green">$</span> npm install <span class="green">-g</span> claps.js</p>
            </div>
          </div>
          <div class="perks">
            <ul>
              <li><i class="far fa-check-circle"></i>Organize your data</li>
              <li><i class="far fa-check-circle"></i>Work with any team</li>
            </ul>
          </div>
        </div>
      </section>

      <!-- sect build tools -->
      <section class="build-tools">
        <div class="bt-left-info">
          <h2>Build tools and extensive documention</h2>
          <p>You can combine all the Landrick templates into a singole one, you can take a component from the Application Theme and use it in the Website</p>
          <ul>
            <li><i class="far fa-check-circle"></i>Digital Marketing Solutions for Tomorrow</li>
            <li><i class="far fa-check-circle"></i>Our Talented & Experienced Marketing Agency</li>
            <li><i class="far fa-check-circle"></i>Create your own skin to match your brand</li>
          </ul>
          <div class="btn btn-dark">
            Read More <i class="fas fa-arrow-right"></i>
          </div>
        </div>
        <div class="bt-right-image">
          <img src="../assets/img/1.png" alt="">
        </div>
      </section>
      <div class="mid-section-rates">
        <h2>Our rates for developer from landrick team</h2>
        <p>Start working with <span class="blue">Landrick</span> that can provide everything you need to generate awareness, drive traffic, connect.</p>
      </div>

      <!-- sect plans -->
      <section class="plans">
        <PlansCard 
        v-for="(item, index) in plansCardInfo" 
        :key="`plansCard${index}`"
        :cardInfo="item"/>
      </section>
      
      <!-- sect newsletter -->

    </div>
  </main>
</template>

<script>

import KeyfeaturesCard from './KeyfeaturesCard.vue'
import PlansCard from './PlansCard.vue'

export default {
  name: 'Main',
  components: {
    KeyfeaturesCard,
    PlansCard
  },
  data(){
    return{
      kfCardInfo: [
        'modular',
        'responsive',
        'customizable',
        'scalable'
      ],
      plansCardInfo: [
        {
          label: 'Basic',
          price: '9.00',
          description: 'All the basics for businesses that are just getting started.',
          isBestDeal: false
        },
        {
          label: 'Business',
          price: '39.00',
          description: 'Better for growing businesses that want more customers.',
          isBestDeal: true
        },
        {
          label: 'Enterprise',
          price: '79.00',
          description: 'Advanced features for pros who need more customization.',
          isBestDeal: false
        },
      ]
    }
  }
}
</script>

<style lang="scss">
@import '../assets/style/vars.scss';

  .container {
    width: 60%;
    margin: 0 auto;
    h2 {
      padding: 30px 0;
      font-size: 36px;
      font-weight: 400;
    }
    .blue {
      color: $menu-dark-bg !important;
      padding: 0 !important;
    }
    section.key-features {
      padding: 80px 0 50px 0;
      .kf-text {
        width: 50%;
        p {
          color: $light-text-color;
          margin-bottom: 50px;
        }
      }
      .kf-cards {
        display: flex;
        gap: 30px;
      }
    }
    section.quickstart {
      padding-top: 50px;
      display: flex;
      flex-direction: column;
      align-items: center;
      .qs-text {
        text-align: center;
        width: 50%;
        p {
          color: $light-text-color;
          padding-bottom: 50px;
        }
      }
      .qs-graph {
        background-color: $blueish-dark-bg;
        padding: 20px;
        border-radius: 5px;
        ul {
          display: flex;
          background-color: $dark-grey-bg;
          border: 1px solid $dark-grey-bg;
          border-radius: 5px;
          li {
            padding: 5px 60px;
            color: #fff;
            font-size: 18px;
            &:first-child {
              background-color: $blueish-dark-bg;
              border-radius: 5px;
            }
          }
        }
        .graph-cmd {
          p {
            color: lighten($dark-grey-bg, 30);
            padding: 10px 0;
            span.green {
              color: #2ECA8B;
            }
          }
        }
      }
      .perks {
        ul  {
          display: flex;
          li {
            padding: 10px 50px 0 0;
            color: $light-text-color;
            i {
              padding-right: 5px;
              color: #2ECA8B;
            }
          }
        }
      }
    }
    section.build-tools {
      display: flex;
      align-items: center;
      justify-content: space-between;
      padding-top: 100px;
      .bt-left-info {
        width: 50%;
        margin-right: 50px;
        h2 {
          width: 65%;
          padding: 0;
        }
        p {
          padding: 30px 0;
        }
        p, li {
          color: $light-text-color;
        }
        li {
          padding: 5px 0;
          i {
          color: $active-link-color;
          padding-right: 10px;
          }
        }
        .btn {
          margin: 20px 0;
          i {
            font-size: 12px;
          }
        }
      }
      .bt-right-image {
        img {
          width: 500px;
        }
      }
    }
    .mid-section-rates {
      width: 60%;
      margin: 0 auto;
      text-align: center;
      padding-top: 70px;
      p {
        color: $light-text-color;
      }
    }
    section.plans {
      display: flex;
      gap: 30px;
    }
  }
</style>