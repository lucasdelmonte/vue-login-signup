<template>
  <div class="gallery__image">
    <img v-for="(url, index) in images" :src="url" :key="index" alt="Image" />
  </div>
</template>

<script setup lang="ts">
  const { images } = defineProps(["images"])
</script>

<style scoped lang="scss">
  .gallery {
    &__image {
    flex: 0 0 29%;
    width: 29%;
    object-fit: cover;
    scroll-snap-align: center;
    display: flex;
    gap: 0 0.8rem;

    img {
      width: 100%;
      object-fit: contain;
    }
  }
  }
</style>