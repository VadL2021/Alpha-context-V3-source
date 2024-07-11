<template>
  <h1 class="title">
    {{ titleText }}
  </h1>
</template>

<script>
export default {
  name: 'TitleView',
  props:{
    titleText: {
      type: String,
      require: true  
    }
  }
}
</script>

<style lang="scss" scoped>
    @import "./title"
</style>