<template>
  <div class="header">
    <button class="settings mobile-only" >
      
    </button>
    <img class="logo mobile-only" 
      src="./1.webp"
    >
    <img class="logo desktop-only" 
      src="./1.svg"
    >
    <div class="wrapper links-wrapper desktop-only ">
      <a class="navigation-link desktop-only"
        href=""
      >
        ГЛАВНАЯ  
      </a>
      <a class="navigation-link desktop-only"
        href=""
      >
        ДОМА  
      </a>
      <a class="navigation-link desktop-only"
        href=""
      >
        БАНИ  
      </a>
    </div>
    <div class="wrapper contacts-wrapper">
      <div class="contract-line">
        <TextView class="city desktop-only"
          :text="'Санкт-Петербург:'"
        />
        <TextView class="phone-number"
          :text="'8 (812) 603-72-22'"
        />
      </div> 
      <div class="contract-line">
        <TextView class="city desktop-only"
          :text="'Москва:'"
        />
        <TextView class="phone-number"
          :text="'8 (499) 380-77-33'"
        />
      </div>
    </div>
  </div>
</template>

<script>
import TextView from './text/text.vue'
export default {
  name: 'HeaderView',
  components: {
    TextView
  }
}
</script>

<style lang="scss" scoped>
  @media (max-width: 991px) {
    @import "./header-mobile";
  }
  @media (min-width: 992px) {
    @import "./header";
  }
  @import url("./wrapper.scss");
</style>