<template>
  <HeaderView class="header"/>
  <MainView class="main"/>
  <FooterView class="footer"/>
</template>

<script>
import MainView from "./common.blocks/main/main.vue"
import FooterView from "./common.blocks/footer/footer.vue"
import HeaderView from "./common.blocks/header/header.vue"

export default {
  name: 'App',
  components: {
    MainView,
    FooterView,
    HeaderView
  }
}
</script>

<style lang="scss" scoped>
  @import "./App";
</style>
