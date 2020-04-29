<script>
  import Swiper from './core.js';
  import { onMount } from 'svelte';
  export let autoPlay = true;
  export let duration = 500;
  export let interval = 2500;
  export let showIndicator = true;

  let swiperElement;

  $: if(swiperElement) {
    new Swiper({
      selector: swiperElement
    })
  }
</script>

<div class="swiper" bind:this={swiperElement}>
  <slot></slot>
</div>

<style lang="scss">
.swiper {
  
}
</style>