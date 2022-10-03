<template>
  <div class="container">
    <slot />
  </div>
</template>

<script setup lang="ts">
interface Props {
  size: string
};

const props = defineProps<Props>();
</script>

<style scoped>
.container {
  width: 100%;
  max-width: v-bind(size);
  margin-left: auto;
  margin-right: auto;
  padding-left: var(--size-32);
  padding-right: var(--size-32);
}
</style>
