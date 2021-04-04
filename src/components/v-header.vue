<template>
  <nav class="navbar navbar-expand-lg navbar-light">
    <div class="container">
      <a class="navbar-brand logo" href="/"><img src="../assets/images/icons/logo.png" alt=""></a>
      <div class="collapse collapse-fontsize navbar-collapse" id="navbarSupportedContent">
        <ul class="navbar-nav mr-auto mb-2 mb-lg-0">
          <li
            class="nav-item menu-link"
            v-for="(menu, index) in headerMenuList"
            :key="index"
            :class="isActiveClassHadnler(menu.path)"
          >
            <router-link class="nav-link" aria-current="page" :to="menu.path" exact>
              {{ menu.name }}
            </router-link>
          </li>
        </ul>
        <div class="icons">

          <a href="https://www.facebook.com/" target="_blank"><img src="../assets/images/icons/f.png" alt=""/></a>
          <a href="https://www.pinterest.ru/" target="_blank"><img src="../assets/images/icons/p.png" alt=""/></a>
          <a href="https://www.instagram.com/" target="_blank"><img src="../assets/images/icons/insta.png" alt=""/></a>
          <a href="https://myaccount.google.com/" target="_blank"><img src="../assets/images/icons/g+.png" alt=""/></a>
        </div>
      </div>
    </div>
  </nav>
</template>

<script>
import {menuList} from '../constants/menuLinks'

export default {
  name: 'v-header',
  props: {
    msg: String
  },
  data() {
    return {
      headerMenuList: menuList
    }
  },
  methods: {
    isActiveClassHadnler(link) {
      return link === this.$route.path ? 'header__isActive' : ''
    },
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss">
@import "../assets/layouts/index";

.navbar {
  height: 90px;
  padding: 0;

  .nav-link {
    white-space: nowrap;
  }
}

.header__isActive {
  background: $greyLight;
}

.navbar-nav {
  height: 90px;
}
.logo {
  padding-right: 180px;
}
.collapse-fontsize {
  font-size: 18px;
}
.menu-link {
  padding: 25px 30px;

  &:hover {
    background: $greyLight;
  }
}

.icons {
  width: 180px;
  a {
    width: 30px;
    height: 30px;
    text-align: center;
    border: 1px solid $greyLight;
    border-radius: 50%;
    margin-right: 10px;
    display: inline-block;
  }
}
</style>
