<template>
  <div class="main">
    <IntroView class="intro"/>
    <AboutView class="about"/>
    <UnitSelectionView class="unit-slector" />
    <AdvantegesView class="advantages" />
    <GalleryView class="gallery" />
    <CareerView class="career" />
    <InvitationView class="invitation"/>
  </div>
</template>

<script>
import IntroView from "./intro/intro.vue"
import AboutView from "./about/about.vue"
import UnitSelectionView from "./unit-slector/unit-selector.vue"
import AdvantegesView from './advantages/advantages.vue'
import GalleryView from './gallery/gallery.vue'
import CareerView from './career/career.vue'
import InvitationView from './invitation/invitation.vue'
export default {
  name: 'MainView',
  components: {
    IntroView,
    AboutView,
    UnitSelectionView,
    AdvantegesView,
    GalleryView,
    CareerView,
    InvitationView
  }
}
</script>

<style lang="scss" scoped>
  @media (max-width: 992px) {
    @import "./main-mobile";
  }
  @media (min-width: 992px) {
    @import "./main";
  }
</style>
