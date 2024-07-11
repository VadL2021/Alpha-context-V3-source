<template>
  <div class="advantages">
    <TitleView  class="title"
      :titleText="'ПРЕИМУЩЕСТВА КОМПАНИИ'"
    />
    <div class="cards-wrapper">
      <AdvantagesCardView 
        :icon="require('./1.svg')"
        :advantage="'Качество продукта'"
        :details="`Мы гордимся результатами своей работы! 
          Мы убеждены, что именно качество 
          — это самое главное, это то, 
          что даёт Нам уверенность в завтрашнем дне.`"
      />
      <AdvantagesCardView 
        :icon="require('./2.svg')"
        :advantage="'Популярность бренда в сети'"
        :details="`Мы занимаем высокие позиции в поисковой 
          выдаче и имеем многочисленные отзывы, 
          привлекающие новых заказчиков независимо 
          от времени года.`"
      />
      <AdvantagesCardView 
        :icon="require('./3.svg')"
        :advantage="'Передовое рабочее место'"
        :details="`Комфортный офис в центре г. Санкт-Петербург, 
          оборудованный передовыми технологиями. 
          Твой рабочий компьютер может быть даже 
          в твоём смартфоне!`"
      />
      <AdvantagesCardView 
        :icon="require('./4.svg')"
        :advantage="'Свои автоматизированные системы обучения'"
        :details="`Создали и постоянно улучшаем собственные 
          автоматизированные системы обучения 
          специалистов и повышения их квалификации 
          внутри компании.`"
      />
      <AdvantagesCardView 
        :icon="require('./5.svg')"
        :advantage="'Сотрудничество с ведущими Компаниями рынка'"
        :details="`Сотрудничаем с ведущими Компаниями рынка 
          строительных материалов: «Grand Line», «Петрович», 
          «Окна Петербурга», «КраскиДоски», «Technonicol» 
          и другими.`"
      />
    </div>
  </div>
</template>

<script>
import TitleView from "./title/title.vue"
import AdvantagesCardView from "./advantages-card/advantages-card.vue"
export default {
  name: 'AdvantegesView',
  components: {
    TitleView,
    AdvantagesCardView
  }
}
</script>

<style lang="scss" scoped>
  @media (max-width: 992px) {
    @import "./advantages-mobile";
  } 
  @media (min-width: 992px) {
    @import "./advantages";
  } 
  @import url(./wrapper.scss);
</style>