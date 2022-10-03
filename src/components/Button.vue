<template>
  <button class="button" :type="props.type">
    <slot />
  </button>
</template>

<script setup lang="ts">
import type { ButtonHTMLAttributes } from 'vue';

interface Props {
  type: ButtonHTMLAttributes['type']
}

const props = withDefaults(defineProps<Props>(), {
  type: 'button'
});
</script>

<style scoped>
.button {
  min-width: 11.25rem;
  padding: var(--size-16);
  background: var(--gradient-light);
  border: 0;
  border-radius: var(--size-16);
  color: var(--color-dark);
  border: 0;
  text-transform: lowercase;
  font-weight: bold;
  font-size: var(--size-20);
  will-change: scale;
  transition: scale var(--ease-elastic-1) var(--time-3);
}

@media (hover) {
  .button:hover {
    scale: 1.1;
    cursor: pointer;
  }
}
</style>