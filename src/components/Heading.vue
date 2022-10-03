<template>
  <component v-bind:is="`h${props.level}`" class="heading">
    <slot />
  </component>
</template>

<script setup lang="ts">
interface Props {
  level: '1' | '2' | '3' | '4' | '5' | '6'
};

const props = defineProps<Props>();
</script>

<style scoped>
.heading {
  text-shadow: 0px var(--size-4) var(--size-4) rgba(29, 49, 84, 0.1);
}

h1,
h2 {
  font-size: clamp(var(--size-48), calc(1rem + 6vw), var(--size-60));
  line-height: 1.2;
  font-weight: 900;
  margin-bottom: var(--size-20);
}

h1 {
  margin-bottom: var(--size-20)
}

h2 {
  margin-bottom: var(--size-60)
}

h3 {
  font-size: clamp(var(--size-18), calc(1rem + 6vw), var(--size-20));
  font-weight: 700;
}

h4 {
  font-size: 1rem;
  font-weight: 600;
}
</style>