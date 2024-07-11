<template>
  <div class="gallery-items">
    <div class="items-wrapper">
      <img class="item_left"
        v-if="currentGalleryElement > 1"
        :src="itemList[currentGalleryElement-1]" 
      >
      <img class="item_middle"
        :src="itemList[currentGalleryElement]" 
      > 
      <img class="item_right"
      v-if="currentGalleryElement != galleryElementAmountLimit"
        :src="itemList[currentGalleryElement+1]" 
      >
    </div>
  </div>
</template>

<script>
export default {
  name: 'GalleryItemsView',
  props: {
    currentGalleryElement: {
      type: Number,
      require: true
    },
    galleryElementAmountLimit: {
      type: Number,
      require: true   
    },
    imgAdresses: {
      type: Array,
      require: true    
    }
  },
  data() {
    return{
      itemList: {}
    }
  },
  mounted(){
    if (this.galleryElementAmountLimit > 0){
      let maxElementAmount = this.galleryElementAmountLimit
      while (maxElementAmount > 0) {
        this.itemList[maxElementAmount] = this.imgAdresses[maxElementAmount-1] 
        maxElementAmount-=1
      }
    } else {
      console.log('Amout of elements cant be less than 0!')
    }
  }
}
</script>

<style lang="scss" scoped>
  @media (max-width: 991px) {
      @import "./gallery-items-mobile";
  } 
  @media (min-width: 992px) {
      @import "./gallery-items.scss";
  } 
</style>