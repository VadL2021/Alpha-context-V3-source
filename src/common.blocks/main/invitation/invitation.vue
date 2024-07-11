<template>
  <div class="invitation">
    <div class="wrapper invitation-wrapper">
      <TitleView class="title"
        :titleText="`НАШИ УСПЕХИ — ЭТО 
        ЗАСЛУГА ЗАМЕЧАТЕЛЬНЫХ ЛЮДЕЙ, 
        РАБОТАЮЩИХ В НАШЕЙ КОМАНДЕ.`"
      />
      <TitleView class="title"
        :titleText="`У НАС ВСЕГДА ЕСТЬ ВАКАНСИИ 
        ДЛЯ СИЛЬНЫХ КАНДИДАТОВ`"
      />
    </div>
    <div class="wrapper form-link-wrapper">
      <TextView class="text"
        :text="`Если чувствуешь в Себе потенциал 
          и здоровые амбиции — ждём рядом с Нами!`"
      />
      <ButtonView class="button"
        :buttonText="'Присоединиться к команде'"
      />
    </div>
  </div>
</template>

<script>
import TitleView from './title/title.vue'
import TextView from './text/text.vue'
import ButtonView from "./button/button.vue"
export default {
  name:'InvitationView',
  components:{
    TitleView,
    TextView,
    ButtonView
  }
}
</script>

<style lang="scss" scoped>
  @media (max-width: 991px) {
    @import "./invitation-mobile";
  }
  @media (min-width: 992px) {
    @import "./invitation";
  }
  @import url(./wrapper.scss);
</style>