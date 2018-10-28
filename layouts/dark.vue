<template>
  <div class="h-screen text-grey-lightest bg-grey-darkest">
    <div class="main">
      <nuxt />
    </div>
    <map-world></map-world>
  </div>
</template>

<script>
import MapWorld from '@/components/map';
export default {
  components: {
    MapWorld
  }
};
</script>

<style>
.main {
  z-index: 100;
  position: relative;
}
</style>

