<script>
  import Swiper from './core.js';
  import { onMount } from 'svelte';
  export let autoPlay = true;
  export let duration = 500;
  export let interval = 2500;
  export let startIndex = 0;
  export let showIndicator = true;
  export let swiperHeight = 300; //px
  export let adaptive = false;  //是否适应屏幕

  let ready;
  let swiperElement;
  $: ready = !!swiperElement;
  
  $: if(ready) {
    new Swiper({
      selector: swiperElement,
      autoPlay,
      duration,
      interval,
      startIndex,
      showIndicator,
    })
  }
</script>

<div class="swiper" bind:this={swiperElement}>
  <slot></slot>
</div>

<style lang="scss">
.swiper {
  height: 500px;
}
</style>