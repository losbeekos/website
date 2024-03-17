<template>
  <label class="form-label">
    <slot />
    <div v-if="optional" class="optional">
      (optioneel)
    </div>
  </label>
</template>

<script setup lang="ts">
interface Props {
  optional?: boolean;
};

defineProps<Props>();
</script>

<style scoped>
.form-label {
  display: flex;
  justify-content: space-between;
  font-weight: bold;
  font-size: var(--size-18);
  padding: var(--size-12) var(--size-24);
  text-shadow: var(--text-shadow);
}

.optional {
  font-weight: 500;
  font-size: var(--size-16);
}
</style>