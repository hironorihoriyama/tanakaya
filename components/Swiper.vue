<template>
  <div v-swiper:mySwiper="swiperOption">
    <div class="swiper-wrapper">
      <div class="swiper-slide swiper-slide_01"></div>
      <div class="swiper-slide swiper-slide_02"></div>
    </div>
  </div>
</template>

<script>
import { Swiper, SwiperSlide, directive } from 'vue-awesome-swiper'
import 'swiper/css/swiper.css'

export default {
  components: {
    Swiper,
    SwiperSlide
  },
  directives: {
    swiper: directive
  },
  data() {
    return {
      swiperOption: {
        width: 303,
        speed: 1000,
        loop: true,
        effect: 'slide',
        spaceBetween: 10,
        breakpoints: {
          768: {
            width: 500,
            spaceBetween: 70,
          },
        }
      },
    }
  }
}
</script>

<style　lang="sass">
@import '~assets/scss/_mixin.scss';
.swiper
  &-container
    height: 416px
    @include mediaQuery-down(sm)
      height: 252px
  &-slide
    background-size: cover
    background-position: center
    &_01
      background-image: url('~@/assets/img/ss1.jpg')
    &_02
      background-image: url('~@/assets/img/ss2.jpg')
</style>
