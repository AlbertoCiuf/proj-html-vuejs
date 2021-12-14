<template>
  <div class="kf-card">
    <div class="icon">
      <i v-if="cardInfo==='modular'" class="fas fa-layer-group"></i>

      <i v-else-if="cardInfo==='responsive'" class="fas fa-external-link-alt"></i>

      <i v-else-if="cardInfo==='customizable'" class="far fa-plus-square"></i>

      <i v-else class="fas fa-expand-arrows-alt"></i>
    </div>
    <div class="card-title">
      <h4>{{cardInfo}}</h4>
    </div>
    <div class="description">
      Composed in a pseudo-Latin language which more or less corresponds.
    </div>
    <div class="read-more">
      <a href="#">Read More <i class="fas fa-chevron-right"></i> </a>
    </div>
  </div>
</template>

<script>
export default {
  name: 'KeyfeaturesCard',
  props: {
    cardInfo: String
  }
}
</script>

<style lang="scss" scoped>
@import '../assets/style/vars.scss';

  .kf-card {
    width: calc(100% / 4);
    border: 1px solid lighten($light-text-color, 30);
    border-radius: 5px;
    padding: 15px;
    .icon i {
      font-size:20px;
      background-color: $menu-light-bg;
      color: $active-link-color;
      padding: 15px;
      border-radius: 5px;
    }
    .card-title h4 {
      text-transform: capitalize;
      font-weight: 400;
      padding: 20px 0 5px 0;
    }
    .description {
      color: $light-text-color;
      padding-bottom: 15px;
    }
    .read-more > * {
      color: $active-link-color;
      & > i {
        font-size: 12px;
      }
    }

  }
</style>