<template>
  <button class="button">
    <p class="button-text">
      {{ buttonText }}
    </p>
  </button>
</template>

<script>
export default {
  name: 'ButtonView',
  props:{
    buttonText:{
      type: String,
      require: true
    }
  }
}
</script>

<style lang="scss" scoped>
    @import "./button"
</style>