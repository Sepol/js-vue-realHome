<template>
  <footer class="footer footer_bg">
    <div class="container">
      <div class="row">
        <v-footer-icons />
        <v-footer-navigation :footerMenu="footerMenu"/>
        <v-footer-client :footerMenuClient="footerMenuClient"/>
        <v-footer-contacts />
      </div>
    </div>
  </footer>
</template>

<script>
import {menuList, menuClient} from '../../constants/menuLinks'

import VFooterIcons from "./v-footer-icons";
import VFooterNavigation from "./v-footer-navigation";
import VFooterClient from "./v-footer-client";
import VFooterContacts from "./v-footer-contacts";
export default {
  name: "v-footer",
  data() {
    return {
      footerMenu: menuList,
      footerMenuClient: menuClient
    }
  },
  components: {
    VFooterContacts,
    VFooterClient,
    VFooterNavigation,
    VFooterIcons
  },
}
</script>

<style scoped>

</style>