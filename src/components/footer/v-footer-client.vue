<template>
  <div class="col">
    <h3 class="footer__title">Navigation</h3>
    <ul class="footer__list">
      <li class="footer__item footer__list_capitalize" v-for="({ name, path }, i) in footerMenuClient" :key="i">
        <router-link :to="path" class="footer__link">{{ name }}</router-link>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "v-footer-client",
  props: {
    footerMenuClient: {
      type: Array,
      required: true,
    }
  }
}
</script>

<style scoped>

</style>