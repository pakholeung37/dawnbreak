<script>
import Swiper from '../components/modules/swiper/Swiper.svelte';
import SwiperSlide from '../components/modules/swiper/Slide.svelte';
</script>

<Swiper>
  <SwiperSlide>
    <div class="slide slide-1">red</div>
  </SwiperSlide>
  <SwiperSlide>
    <div class="slide slide-2">blue</div>
  </SwiperSlide>
  <SwiperSlide>
    <div class="slide slide-3">green</div>
  </SwiperSlide>
</Swiper>

<style lang="scss">
.slide {
  width: 100%;
  height: 100%;
  display: flex;
  justify-content: center;
  align-content: center;
  &-1 {
    background: red;
  }
  &-2 {
    background: blue;
  } 
  &-3 {
    background: green;
  }
}

</style>