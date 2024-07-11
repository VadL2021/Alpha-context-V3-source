<template>
  <div class="footer">
    <div class="wrapper footer-wrapper">
      <div class="contacts-wrapper">
        <TitleView  class="title"
          :titleText="'КОНТАКТЫ'"
        />
        <div class="wrapper switch-wrapper">
          <SwitchView class="switch"
            :switchText="'САНКТ-ПЕТЕРБУРГ'"
            :switchNumber="1"
            :selectedSwitchNumber="currentSwitch"
            @switch-select="currentSwitch = 1"
          />
          <SwitchView class="switch"
            :switchText="'МОСКВА'"
            :switchNumber="2"
            :selectedSwitchNumber="currentSwitch"
            @switch-select="currentSwitch = 2"
          />
        </div>
        <div class="wrapper wrapper-contact-info">
          <div class="wrapper wrapper-contact-item">
            <img class="image"
              src="./2.svg"
            >
            <TextView class="text" 
              :text="'8 (812) 602-77-60'"
            />
          </div>
          <div class="wrapper wrapper-contact-item">
            <img class="image"
              src="./3.svg"
            >
            <TextView class="text" 
              :text="`info@pplk.ru`"
            />
          </div>
          <div class="wrapper wrapper-contact-item">
            <img class="image"
              src="./4.svg"
            >
            <TextView class="text_underlined" 
              :text="`ул. Заозёрная, д. 8 к. 2, офис 202 (7 мин. пешком от метро Фрунзенская)`"
            />
          </div>
          <div class="wrapper wrapper-media">
            <img class="media-ico" 
              src="./5.svg"
            >
            <img class="media-ico" 
              src="./6.svg"
            >         
            <img class="media-ico" 
              src="./7.svg"
            > 
          </div>
        </div>
      </div>
      <img class="map mobile-only" 
        src="./1.webp"
      >
      <img class="map desktop-only" 
        src="./1.svg"
      >
    </div>
    <div class="wrapper copyright-wrapper">
      <TextView class="text copyrigth"
        :text="`© 2023 Пестовский Лесокомбинат. 
          Все права защищены. `"
      />
      <TextView class="text copyrigth desktop-only"
        :text="`Оформить 
          заявку на кредит`"
      />
      <br class="mobile-only">
      <TextView class="text_underlined copyrigth"
        :text="`Реквизиты`"
      />
      <TextView class="text_underlined copyrigth"
        :text="`Политика конфиденциальности`"
      />
    </div>
    <img class="logo" 
      src="./8.svg"
    >
  </div>
</template>

<script>
import TitleView from './title/title.vue'
import TextView from './text/text.vue'
import SwitchView from './switch/switch.vue'
export default {
  name: "FooterView",
  components: {
    TitleView,
    TextView,
    SwitchView
  },
  data() {
    return {
      currentSwitch: 0
    }
  }
}
</script>

<style lang="scss" scoped>
  @media (max-width: 992px) {
    @import "./footer-mobile";
  }
  @media (min-width: 992px) {
    @import "./footer";
  }
  @import url(./wrapper.scss)
</style>