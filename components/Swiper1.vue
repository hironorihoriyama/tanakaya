<template>
  <div v-swiper:mySwiper="swiperOption">
    <div class="swiper-wrapper">
      <div class="swiper-slide swiper-slide_1_1"></div>
      <div class="swiper-slide swiper-slide_1_2"></div>
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
    &_1
      &_1
        background-image: url('~@/assets/img/ss11.jpg')
        @include retina
          background-image: url('~@/assets/img/ss11@2x.jpg')
      &_2
        background-image: url('~@/assets/img/ss12.jpg')
        @include retina
          background-image: url('~@/assets/img/ss12@2x.jpg')
</style>
