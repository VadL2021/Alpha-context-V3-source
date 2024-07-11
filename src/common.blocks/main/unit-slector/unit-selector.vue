<template>
  <div class="unit-selector">
    <TitleView class="title"
      :titleText="'ВЫБЕРИ ПОДРАЗДЕЛЕНИЕ:'"
    />
    <div class="unit-selection__panel">
      <SwitchView class="switch"
        :switchText="'СТРОИТЕЛЬНЫЙ ОТДЕЛЬ'"
        :switchNumber="1"
        :selectedSwitchNumber="currentSwitch"
        @switch-select="currentSwitch = 1"
      />
      <SwitchView class="switch"
        :switchText="'ОФИС'"
        :switchNumber="2"
        :selectedSwitchNumber="currentSwitch"
        @switch-select="currentSwitch = 2"
      />
      <SwitchView class="switch"
        :switchText="'ФИНАНСОВЫЙ ОТДЕЛ'"
        :switchNumber="3"
        :selectedSwitchNumber="currentSwitch"
        @switch-select="currentSwitch = 3"
      />
      <SwitchView class="switch"
        :switchText="'ОТДЕЛ ПРОДАЖ'"
        :switchNumber="4"
        :selectedSwitchNumber="currentSwitch"
        @switch-select="currentSwitch = 4"
      />
      <SwitchView class="switch"
        :switchText="'ВНЕШТАТНЫЙ СОТРУДНИК'"
        :switchNumber="5"
        :selectedSwitchNumber="currentSwitch"
        @switch-select="currentSwitch = 5"
      />
    </div>
    <div class="wrapper cards-wrapper">
      <JobCardView class="job-card"
        :position="'Прораб'"
        :salary="'ОТ 00 000 РУБ'"
      />
      <JobCardView class="job-card"
        :position="'Специалист службы снабжения'"
        :salary="'ОТ 00 000 РУБ'"
      />
      <JobCardView class="job-card"
        :position="'Логист'"
        :salary="'Обсуждается на собеседовании'"
      />
      <JobCardView class="job-card"
        :position="'Проектировщик'"
        :salary="'ОТ 00 000 РУБ'"
      />
    </div>
    <ButtonView class="button"
      :buttonText="'ОТКЛИКНУТЬСЯ НА ВАКАНСИЮ'"
    />
  </div>
</template>

<script>
import TitleView from "./title/title.vue"
import SwitchView from "./switch/switch.vue"
import JobCardView from "./job-card/job-card.vue"
import ButtonView from "./button/button.vue"
export default {
  name: 'UnitSelectionView',
  components:{
    TitleView,
    SwitchView,
    JobCardView,
    ButtonView
  },
  data() {
    return {
      currentSwitch: 0
    }
  },
  methods:{
    moveNumberOne(){
      this.currentSwitch=1; 
      console.log('clicked')
    }
  }
}
</script>
    
<style lang="scss" scoped>
  @media (max-width: 991px) {
    @import "./unit-selector-mobile";
  }
  @media (min-width: 992px) {
    @import "./unit-selector";
  }

  @import url(wrapper.scss);
</style>