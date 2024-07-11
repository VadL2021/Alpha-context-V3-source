<template>
  <div class="position-index">
    <p>{{elementsNumber}}</p>
    <div class="image-wrapper"
        v-for="(el, index) in elementsArray" :key="index"
    >
        <img  class="image"
            v-if="currentGalleryElement != index+1"
            src="./1.svg" 
        >
        <img  class="image"
            v-if="currentGalleryElement == index+1"
            src="./2.svg" 
        >
    </div>
  </div>
</template>

<script>
export default {
    name: 'PositionIndexView',
    props: {
        currentGalleryElement: {
            type: Number,
            require: true
        },
        galleryElementAmountLimit: {
            type: Number,
            require: true
        }
    },
    data() {
        return {
            elementsArray: []
        }
    },
    mounted(){
        let elementsNumber = this.galleryElementAmountLimit
        while (elementsNumber > 0){
            this.elementsArray.push(elementsNumber)
            // console.log(this.elementsArray)
            elementsNumber-=1
        }
        this.elementsArray.reverse()
        // console.log(this.elementsArray)
    }

}
</script>

<style lang="scss" scoped>
    
    @media (max-width: 991px) {
        @import './position-index-mobile';
    } 
    @media (min-width: 992px) {
        @import './position-index';
    } 
</style>