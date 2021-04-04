<template>
  <v-main-container>
    <template v-slot:header>
      <v-header/>
    </template>
    <main>
      <router-view/>
    </main>
    <template v-slot:footer>
      <v-footer/>
    </template>
  </v-main-container>
</template>

<script>
// @ is an alias to /src
import vHeader from './components/v-header'
import vFooter from './components/footer/v-footer'
import VMainContainer from "./components/v-main-container";

export default {
  name: 'Home',
  components: {
    VMainContainer,
    vHeader,
    vFooter
  }
}
</script>
