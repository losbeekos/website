<template>
  <picture class="avatar">
    <!-- <source srcset="/images/avatar.avif" type="image/avif" /> -->
    <img class="image" src="/images/avatar.webp" width="144" height="144" fetchpriority="high" alt="Jeroen van Beek portrait" />
  </picture>
</template>

<style scoped>
.avatar {
  display: inline-block;
  margin-top: var(--size-32);
  border-radius: 50%;
  overflow: hidden;
}

.image {
  max-width: clamp(6rem, calc(1rem + 16vw), 9rem);
  height: auto;
}
</style>