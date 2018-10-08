<template lang="pug">
  swiper(
    :options="swiperOption"
  )
    swiper-slide
      tumb(
        href="https://ya.ru",
        src="https://images.unsplash.com/photo-1504027973709-58986e840e79?ixlib=rb-0.3.5&ixid=eyJhcHBfaWQiOjEyMDd9&s=2128648cd2f50b4110030bf722eaea59&auto=format&fit=crop&w=1352&q=80"
      )
    swiper-slide Slide 2
    swiper-slide Slide 3
    swiper-slide Slide 4
    swiper-slide Slide 5
    swiper-slide Slide 6
    swiper-slide Slide 7
    swiper-slide Slide 8
    swiper-slide Slide 9
    swiper-slide Slide 10
    .swiper-pagination(slot="pagination")
    .swiper-button-prev(slot="button-prev")
    .swiper-button-next(slot="button-next")
</template>

<script>
import 'swiper/dist/css/swiper.css'
import { swiper, swiperSlide } from 'vue-awesome-swiper'
import Tumb from '@/components/Tumb'

export default {
  name: 'carousel',
  components: {
    swiper,
    swiperSlide,
    Tumb
  },
  data () {
    return {
      swiperOption: {
        slidesPerView: 3,
        spaceBetween: 10,
        grabCursor: true,
        loop: true,
        autoplay: {
          delay: 2500,
          disableOnInteraction: false
        },
        pagination: {
          el: '.swiper-pagination',
          clickable: true
          // type: 'progressbar'
        },
        navigation: {
          nextEl: '.swiper-button-next',
          prevEl: '.swiper-button-prev'
        }
      }
    }
  }
}
</script>

<style lang="scss" scoped>
.swiper-container {
  margin: 50px 10px;
}

.swiper-slide {
  min-height: 200px;
  background-color: #f4f4f4;
  // padding: 10px;
  box-sizing: border-box;
  // cursor: pointer;
  border-radius: 4px;
}

.swiper-pagination {
  margin-top: 4px;
}
</style>
