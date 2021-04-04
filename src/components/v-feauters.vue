<template>
  <div class="feature">
    <div class="container">
      <div class="row">
        <div class="col-md-3" v-for="item in data" :key="item.id">
          <div class="feature__col feature__col_pad">
            <img :src="require(`../assets/images/icons/${item.icon}.png`)" class="feature__icon" :alt="item.title">
            <h4 class="feature__title">{{ item.title }}</h4>
            <p class="feature__desc">{{ item.text }}</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "v-feauters",
  props: {
    data: {
      type: Array,
      default: () => [],
    }
  }
}
</script>

<style scoped>

</style>