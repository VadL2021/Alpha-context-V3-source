<template>
  <div class="about">
    <TitleView class="title about__title "
      :titleText="'О компании'"
    />
    <div class="wrapper about__wrapper">
      <div class="wrapper about__item-wrapper">
        <img class="about__item-image"
          src="./1.svg" 
        >
        <TextView class="text about__item-text"
          :text="'Города присутствия: Санкт-Петербург и Москва'"
        />
      </div>
      <div class="wrapper about__item-wrapper">
        <img class="about__item-image"
          src="./2.svg" 
        >
        <TextView class="text about__item-text"
          :text="'Лет среди лидеров рынка'"
        />
      </div>      
      <div class="wrapper about__item-wrapper">
        <img class="about__item-image"
          src="./3.svg" 
        >
        <TextView class="text about__item-text"
          :text="'Домов и бань сдаём ежегодно'"
          style="white-space: nowrap"
          /><!--   Не красиво, но на макете это 1 строка -->
      </div>
    </div>
  </div>
</template>

<script>
import TitleView from "./title/title.vue"
import TextView from "./text/text.vue"
export default {
  name: 'AboutView',
  components:{
      TitleView,
      TextView
    }
}
</script>

<style lang="scss" scoped>
  @media (min-width: 992px) {
    @import "./about";   
  }
  @media (max-width: 992px) {
    @import "./about-mobile";
  }
  @import url(wrapper.scss);
</style>