<template>
  <input class="form-input" :type="props.type" :name="props.name" :placeholder="props.placeholder" :required="props.required">
</template>

<script setup lang="ts">
import type { InputHTMLAttributes } from 'vue';

interface Props {
  name?: string,
  type?: InputHTMLAttributes['type'],
  placeholder?: string,
  required?: boolean,
}

const props = withDefaults(defineProps<Props>(), {
  name: '',
  type: 'text',
  placeholder: '',
  required: false,
});
</script>

<style scoped>
.form-input {
  background: var(--color-light);
  box-shadow: 0 var(--size-4) var(--size-32) rgba(0, 0, 0, 0.2);
  border-radius: var(--size-16);
  width: 100%;
  border: 0;
  font-weight: 600;
  padding: var(--size-16) var(--size-24)
}
</style>