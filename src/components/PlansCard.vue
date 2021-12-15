<template>
  <div class="plans-card">
    <div class="ribbon-wrapper"
      :class="{shown : cardInfo.isBestDeal}">
      <div class="ribbon">
        Best
      </div>
    </div>
    <div class="label">
      {{cardInfo.label}}
    </div>
    <h2>${{cardInfo.price}}</h2>
    <small>Per Month</small>
    <p>{{cardInfo.description}}</p>
    <div class="border-bottom"></div>
    <ul>
      <li><i class="far fa-check-circle"></i>Full Access</li>
      <li><i class="far fa-check-circle"></i>Enhanced Security</li>
      <li><i class="far fa-check-circle"></i>Source Files</li>
      <li><i class="far fa-check-circle"></i>1 Domain Free</li>
      <li><i class="far fa-check-circle"></i>Enhanced Security</li>
    </ul>
    <div class="btn btn-dark">Buy Now</div> <br>
    <small>*No credit card required</small>
  </div>
</template>

<script>
export default {
  name: 'PlansCard',
  props: {
    cardInfo: Object
  }
}
</script>

<style lang="scss" scoped>
@import '../assets/style/vars.scss';

.plans-card {
  position: relative;
  width: calc(100%/3);
  border: 1px solid lighten($light-text-color, 30);
  border-radius: 10px;
  padding: 20px;
  box-shadow: 0 2px 5px $light-text-color;
  border-bottom: 4px solid lighten($light-text-color,20);
  margin-bottom: 100px;
  margin-top: 60px;
  transition: all .2s;
  &:hover {
    transform: scale(1.1);
    border-bottom: 4px solid $active-link-color;
  }
  .ribbon-wrapper {
    display: none;
    position: absolute;
    top: -3px;
    right: -3px;
    width: 85px;
    height: 88px;
    overflow: hidden;
    &.shown{
      display: block;
    }
    .ribbon {
      position: relative;
      text-shadow: rgba(255,255,255,0.5) 0px 1px 0px;
      left: -5px;
      top: 15px;
      width: 130px;
      text-align: center;
      color: #fff;
      background-color: #F17425;
      transform: rotate(45deg);
      box-shadow: 0px 0px 5px rgba(0,0,0,0.3);
      // &::before, &::after {
      //   content: '';
      //   border: 3px solid #F17425;
      // }
    }
  }
  p, small, li {
    color: $light-text-color;
  }
  li i {
    color: $active-link-color;
    padding-right: 5px;
  }
  .label {
    font-size: 18px;
    padding: 5px 20px;
  }
  h2 {
    font-size: 40px;
    padding: 15px 0 0 0;
  }
  p {
    padding: 15px 0;
  }
  .border-bottom {
    margin-bottom: 15px;
  }
  ul li {
    padding: 5px 0;
    &:last-child {
      padding-bottom: 15px;
    }
  }
  .btn {
    width: 100%;
    text-align: center;
    margin-left: 0;
    margin-bottom: 15px;
  }
}

</style>