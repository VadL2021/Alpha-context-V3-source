<template>
  <div class="gallery">
    <TitleView  class="title"
        :titleText="'ПРОЕКТЫ КОМПАНИИ'"
    />
    <div class="wrapper switches-wrapper">
        <SwitchView class="switch"
            :switchText="'БАНИ'"
            :switchNumber="1"
            :selectedSwitchNumber="currentSwitch"
            @switch-select="currentSwitch = 1"
         />
        <SwitchView class="switch"
            :switchText="'ДОМА'"
            :switchNumber="2"
            :selectedSwitchNumber="currentSwitch"
            @switch-select="currentSwitch = 2"
        />
    </div>
    <div class="gallery-view-area">
        <GalleryItemsView   class="gallery-items desktop-only"
            :currentGalleryElement="currentGalleryElement"
            :galleryElementAmountLimit="galleryElementAmountLimit"
            :imgAdresses="imgAdresses"
        />
        <GalleryItemsView   class="gallery-items mobile-only"
            :currentGalleryElement="currentGalleryElement"
            :galleryElementAmountLimit="galleryElementAmountLimit"
            :imgAdresses="imgAdressesMobile"
        />
        <button class="left-navigation-button"
            @click="selectPreviousElement()"
        >
            <img class="card__image mobile-only"
            src="./left.webp"
            >
            <img class="card__image desktop-only"
            src="./left.svg"
            >
        </button>
        <button class="right-navigation-button"
            @click="selectNextElement()"
        >
            <img class="card__image mobile-only"
            src="./right.webp"
            >
            <img class="card__image desktop-only"
            src="./right.svg"
            >
        </button>
    </div>
    <PositionIndexView class="gallery-position-index"
        :currentGalleryElement="currentGalleryElement"
        :galleryElementAmountLimit='galleryElementAmountLimit'
    />
  </div>
</template>

<script>
import TitleView from "./title/title.vue"
import SwitchView from "./switch/switch.vue"
import GalleryItemsView from "./gallery-items/gallery-items.vue"
import PositionIndexView from "./position-index/position-index.vue"
export default {
    name: 'GalleryView',
    components: {
        TitleView,
        SwitchView,
        GalleryItemsView,
        PositionIndexView
    },
    data() {
        return {
            currentSwitch: 0,               //Переключатель БАНИ/ДОМА
            currentGalleryElement: 1,       //Номер текущего элемента галлереи
            galleryElementAmountLimit: 5,   //Максимальное число элементов,
            imgAdresses: [                  //Массив с адресами картинок
                require('./1.svg'),
                require('./2.svg'),
                require('./3.svg'),
                require('./4.svg'),
                require('./5.svg')
            ],
            imgAdressesMobile: [                  //Массив с адресами картинок
                require('./1-mobile.webp'),
                require('./2-mobile.webp'),
                require('./3-mobile.webp'),
                require('./4-mobile.webp'),
                require('./5-mobile.webp')
            ],

        }
  },
  methods: {
    selectPreviousElement() {
        if (this.currentGalleryElement > 1) {
            this.currentGalleryElement -= 1;
        }
    },
    selectNextElement() {
        if (this.currentGalleryElement < this.galleryElementAmountLimit) {
            this.currentGalleryElement += 1;
        }
    }
  }
}
</script>

<style lang="scss" scoped>
    @media (max-width: 992px) {
        @import "gallery-mobile";
    } 
    @media (min-width: 992px) {
        @import "./gallery.scss";
    } 
    @import url(./wrapper.scss);
</style>