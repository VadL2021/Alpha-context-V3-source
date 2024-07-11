<template>
  <div class="job-card">
    <div class="wrapper card-item">
      <div class="wrapper card-line">
        <img class="card__image"
          src="./1.svg"
        >
        <TextView class="card__text_type_position"
          :text="position"
        />
      </div>
      <div class="wrapper card-line">
        <img class="card__image"
          src="./2.svg"
        >
        <TextView class="card__text_type_salary"
          :text="salary"
        />
      </div>
      <button class="card__button">
        <img class="card__image"
          src="./3.svg"
        >
      </button>
    </div>
  </div>
</template>

<script>
import TextView from "./text/text.vue"
export default {
    name: 'JobCardView',
    props:{
        position:{
            type: String,
            require: true
        },
        salary:{
            type: String,
            require: true
        }
    },
    components:{
        TextView
    }
}
</script>

<style lang="scss" scoped>
    @media (max-width: 991px) {
      @import './job-card-mobile';
    }
    @media (min-width: 992px) {
      @import './job-card';
    }
    @import url(wrapper.scss);
</style>