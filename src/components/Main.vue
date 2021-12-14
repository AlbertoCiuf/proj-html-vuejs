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
        <div class="qs-graph">
          <ul>
            <li>npm</li>
            <li>nuget</li>
            <li>spm</li>
            <li>github</li>
          </ul>
          <div class="graph-cmd"></div>
        </div>
        <div class="perks">
          <ul>
            <li>Organize your data</li>
            <li>Work with any team</li>
          </ul>
        </div>
      </section>
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
    }
  }
</style>