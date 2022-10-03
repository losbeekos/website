<template>
  <picture class="picture" aria-hidden="true">
    <!-- <source
      media="(orientation: portrait)"
      srcset="/images/background-portrait.avif"
      type="image/avif"
    /> -->
    <source
      media="(orientation: portrait)"
      srcset="/images/background-portrait.webp"
      type="image/webp"
    />
    <!-- <source
      media="(orientation: landscape)"
      srcset="/images/background.avif"
      type="image/avif"
    /> -->
    <source
      media="(orientation: landscape)"
      srcset="/images/background.webp"
      type="image/webp"
    />
    <img class="image" src="/images/background-portrait.webp" fetchpriority="high" alt="" />
  </picture>
</template>

<style scoped>
.picture {
  position: fixed;
  top: 0;
  left: 0;
  z-index: -1;
  pointer-events: none;
}

.image {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  filter: blur(var(--size-40));
}

@media (orientation: landscape) {
  .image {
    object-fit: contain;
    object-position: top left;
  }
}

@media (orientation: portrait) {
  .image {
    object-fit: cover;
  }
}
</style>
