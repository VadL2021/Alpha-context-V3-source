<template>
  <div class="intro">
    <!-- <img  class="__backround-image"
        src="./intro.svg" 
        alt="Картинка на фоне первого элемента страницы"
    > -->
    <div class="wrapper __intro-wrapper">
      <TitleView class="title intro__title"
        :titleText="'«ПЕСТОВСКИЙ ЛЕСОКОМБИНАТ»'"
      />
      <TextView class="text intro__text"
        :text="'Cтань частью нашей команды!'"
      />
    </div>
    <ButtonView class="button"
      :buttonText="'ОТПРАВИТЬ АНКЕТУ'"
    />
  </div>
</template>

<script>
import TitleView from "./title/title.vue"
import TextView from "./text/text.vue"
import ButtonView from "./button/button.vue"
export default {
    name: 'IntroView',
    components:{
      TitleView,
      TextView,
      ButtonView
    }
}
</script>

<style lang="scss" scoped>
  @media (max-width: 991px) {
    @import "./intro-mobile";
  }
  @media (min-width: 992px) {
    @import "./intro";
  }
</style>