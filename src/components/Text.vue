<template>
  <p class="text">
    <slot />
  </p>
</template>

<style scoped>
.text {
  font-size: clamp(var(--size-16), calc(1rem + 0.5vw), var(--size-20));
  font-weight: medium;
  text-shadow: var(--text-shadow);
  margin-bottom: var(--size-24);
}
</style>