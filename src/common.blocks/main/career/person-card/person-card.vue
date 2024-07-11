<template>
  <div class="person-card">
    <div class="wrapper person-info-wrapper">
      <TitleView  class="name"
        :titleText="name"
      />
      <TitleView  class="job"
        :titleText="job"
      />
      <TextView class="info"
        :text="characterInfoFirstLine"
      /><br>
      <TextView class="info"
        :text="characterInfoSecondLine"
      /><br>
      <TextView class="info"
        :text="characterInfoThirdLine"
      />
    </div>
    <img class="photo"
      :src="photo" 
    >
    <img class="underline desktop-only"
      src="./1.svg"
    >
    </div>
</template>

<script>
import TitleView from './title/title.vue'
import TextView from './text/text.vue'
export default {
  name: 'PersonCardView',
  components: {
    TitleView,
    TextView
  },
  props:{
    name: {
      type: String,
      require: true
    },
    job: {
      type: String,
      require: true
    },
    characterInfoFirstLine: {
      type: String,
      require: true
    },
    characterInfoSecondLine: {
      type: String,
      require: true
    },
    characterInfoThirdLine: {
      type: String,
      require: true
    },
    photo: {
      type: String,
      require: true
    }
  }
}
</script>

<style lang="scss" scoped>
  @media (max-width: 991px) {
    @import "./person-card-mobile";
  } 
  @media (min-width: 992px) {
    @import "./person-card";
  } 
  @import url('./wrapper.scss')
</style>