<template>
  <div class="icon-text">
    <component class="icon" :is="iconComponent" />
    <slot />
  </div>
</template>

<script setup lang="ts">
import { computed, defineAsyncComponent } from 'vue';

const props = defineProps({
  icon: String,
});

const iconComponent = computed(() => {
  return defineAsyncComponent(() => import(`./icons/${props.icon}.vue`))
});
</script>

<style scoped>
.icon-text {
  display: flex;
  gap: var(--size-8);
  align-items: center;
}

.icon {
  flex-shrink: 0;
  width: 1.625rem;
  height: 1.625rem;
}
</style>