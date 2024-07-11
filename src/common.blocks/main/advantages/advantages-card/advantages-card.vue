<template>
  <div class="advantages-card">
    <div class="wrapper card-wrapper">
        <img class="icon desktop-only"
          :src="icon" 
        >
        <TextView class="text_upper"
          :text="advantage"
        />
        <TextView class="text_lower desktop-only"
          :text="details"
        />
        <button class="button mobile-only">
          <img class="button__image mobile-only"
            src="./1.svg"
          >
        </button>
    </div>
  </div>
</template>

<script>
import TextView from "./text/text.vue"
export default {
  name: 'AdvantagesCardView',
  components: {
    TextView
  },
  props:{
    advantage: {
      type: String,
      require: true
    },
    details: {
      type: String,
      require: true
    },
    icon: {
      type: String,
      require: true
    }
  }
}
</script>

<style lang="scss" scoped>
  @media (max-width: 991px) {
    @import "./advantages-card-mobile";
  } 
  @media (min-width: 992px) {
    @import "./advantages-card";
  } 
  @import url(./wrapper.scss);
</style>