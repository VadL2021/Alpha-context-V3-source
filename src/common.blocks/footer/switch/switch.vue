<template>
  <button class="switch" :class="{'switch_on': switchIsOn, 'switch_off': !switchIsOn}" 
    @click="$emit('switch-select');"
  >
    {{ switchText }}
  </button>
</template>

<script>
export default {
  name: 'SwitchView',
  props: {
    switchText: {
      type: String,
      require: true
    },
    switchNumber: {
      type: Number,
      require: true
    },
    selectedSwitchNumber: {
      type: Number,
      requier:  true
    }
  },
  data(){
    return {
      switchIsOn: false
    }
  },
  watch: {
    selectedSwitchNumber(value) {
      value==this.switchNumber ? this.switchIsOn = true : this.switchIsOn = false
    }
  }
}
</script>

<style lang="scss" scoped>
    @import "./switch"
</style>