<template>
  <textarea class="form-textarea" :name="props.name" cols="30" rows="6"></textarea>
</template>

<script setup lang="ts">
interface Props {
  name: string,
}

const props = defineProps<Props>();
</script>

<style scoped>
.form-textarea {
  background: var(--color-light);
  box-shadow: 0 var(--size-4) var(--size-32) rgba(0, 0, 0, 0.2);
  border-radius: var(--size-16);
  width: 100%;
  min-height: var(--size-60);
  border: 0;
  font-weight: 600;
  padding: var(--size-16) var(--size-24);
  resize: vertical;
}
</style>