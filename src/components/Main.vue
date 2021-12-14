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
      <!-- sect build tools -->
      <!-- sect plans -->
      <!-- sect newsletter -->

    </div>
  </main>
</template>

<script>

import KeyfeaturesCard from './KeyfeaturesCard.vue'

export default {
  name: 'Main',
  components: {
    KeyfeaturesCard
  },
  data(){
    return{
      kfCardInfo: [
        {
          icon: 'modular'
        },
        {
          icon: 'responsive'
        },
        {
          icon: 'customizable'
        },
        {
          icon: 'scalable'
        }
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
    section.key-features {
      padding: 80px 0 50px 0;
      .kf-text {
        width: 50%;
        h2 {
          padding: 30px 0;
          font-size: 40px;
          font-weight: 400;
        }
        p {
          color: $light-text-color;
          .blue {
            color: $menu-dark-bg;
          }
          margin-bottom: 50px;
        }
      }
      .kf-cards {
        display: flex;
        gap: 30px;
      }
    }
  }
</style>