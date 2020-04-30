<script>
import Swiper, { next, prev } from '../components/modules/swiper/Swiper.svelte';
import Slide from '../components/modules/swiper/Slide.svelte';

let swiperHeight;
let adaptive = false;
</script>

<Swiper height={swiperHeight} {adaptive} loop>
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

<input type="text" bind:value={swiperHeight} />
<button on:click="{() => prev(1)}">prev</button>
<button on:click="{() => next(1)}">next</button>
<button on:click="{() => adaptive = !adaptive}">adaptive: {adaptive ? 'yes': 'no'}</button>

<style lang="scss">
.slide {
  width: 100%;
  height: 200px;
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