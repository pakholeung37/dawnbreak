<script>
import Swiper from '../components/modules/swiper/Swiper.svelte';
import Slide from '../components/modules/swiper/Slide.svelte';
</script>

<Swiper>
  <Slide>
    <div class="slide slide-1">red</div>
  </Slide>
  <Slide>
    <div class="slide slide-2">blue</div>
  </Slide>
  <Slide>
    <div class="slide slide-3">green</div>
  </Slide>
</Swiper>

<style lang="scss">
.slide {
  width: 100%;
  height: 300px;
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