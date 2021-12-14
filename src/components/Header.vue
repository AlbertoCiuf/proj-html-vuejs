<template>
  <header>
    <div class="container">
      <div class="logo">
        <img src="../assets/img/logo-dark.png" alt="Logo dark">
      </div>
      <nav>
        <ul>
          <li v-for="(link, index) in navLinkList" :key="`link${index}`"
            :class="{active : link.isActive}"
            @click="link.isActive = !link.isActive">
            <a :href="link.href">{{link.name}}</a>
            <i class="fas fa-chevron-down"
              :class="{shown : link.isDropDown}"></i>
          </li>
        </ul>
      </nav>
      <div class="header-icons">
        <ul>
          <li><i class="fas fa-search"></i></li>
          <li class="header-right-menu"><i class="fab fa-github"></i></li>
          <li class="header-right-menu"><i class="fab fa-stack-overflow"></i></li>
          <li class="header-right-menu"><i class="far fa-user"></i></li>
        </ul>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  name: 'Header',
  props: {
    navLinkList: Array
  }
}
</script>

<style lang="scss" scoped>
@import '../assets/style/vars.scss';

header {
  height: 70px;
  background-color: $bg-color;
    .container {
      width: 60%;
      height: 100%;
      margin: 0 auto;
      display: flex;
      justify-content: space-between;
      align-items: center;
      .logo{
        cursor: pointer;
        img {
          width: 120px;
        }
      } 
      nav ul {
        display: flex;
        li {
          margin: 0 30px;
          text-transform: uppercase;
          font-size: 14px;
          cursor: pointer;
          &.active, &:hover {
          color: $active-link-color;
          }
          i {
            display: none;
            &.shown{
              display: inline-block;
              font-size: 12px;
              padding-left: 5px;
            }
          }
        }
      }
      .header-icons {
        height: 100%;
        ul {
          height: 100%;
          display: flex;
          align-items: center;
          li {
            cursor: pointer;
            color: $light-text-color;
            padding: 5px 10px;
            margin: 5px;
            font-size: 14px;
            &.header-right-menu{
              color: $active-link-color;
              background-color: $menu-light-bg;
              border-radius: 5px;
              border: 1px solid #2F55D41A;
              box-shadow: 0 5px 5px $menu-light-bg;
              &:hover{
                color: #fff;
                background-color: $menu-dark-bg;
              }         
            }
          }
        }
      }
    }
}


</style>